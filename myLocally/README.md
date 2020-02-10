

把请求封装成Promise版本

module.exports = (url, data) => {
    return new Promise((resolve, reject) =>{

        wx.request({
            url:`https://locally.uieee.com/${url}`,
            success: resolve,
            fail: reject
        })
            })
}

调用
const fetch = require('../../utils/fetch')
    fetch('slides').then(res => {
      this.setData({slides: res.data})
    })

