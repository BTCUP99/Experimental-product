# Experimental-product
var apiUrl = 'https://api.zksync.io/api/v0.2/accounts/' + address;
  try {
    var result = JSON.parse(UrlFetchApp.fetch(apiUrl));
    var balance = result.result.committed.balances[token.toUpperCase()];
    return balance ? balance / Math.pow(10, decimal) : 0;
  } catch (e) {
    console.log('余额获取失败', e);
    return 0;
  }
}
