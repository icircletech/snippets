/***
* Scans a hash and finds any Characters that are non Base64 compatible.
***/
function findNonBase64Characters($data) {
  $base64Alphabet = str_split('ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/=');
  $nonBase64Characters = array_filter(str_split($data), function ($char) use ($base64Alphabet) {
    return !in_array($char, $base64Alphabet, true);
  });

  return $nonBase64Characters;
}

/*****************
* Example usage *
*****************/

/*********************************************
* $nonBase64Chars = findNonBase64Characters($encodedData);
*
* if (!empty($nonBase64Chars)) {
*   echo "Non-base64 characters found: " . implode(', ', $nonBase64Chars) . PHP_EOL;
* } else {
*   echo "The data appears to be base64-compliant." . PHP_EOL;
* }
***********************************************/
