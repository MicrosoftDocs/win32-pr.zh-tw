---
title: 'WM_GET_LICENSE_DATA 結構 (Drmexternals .h) '
description: WM \_ 取得 \_ 授權 \_ 資料結構包含取得 DRM 授權之位置的相關資訊。
ms.assetid: 7e8053d5-f3f5-4519-97f5-6dbd89982f3a
keywords:
- WM_GET_LICENSE_DATA 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WM_GET_LICENSE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f53b6ddfd532710e712637c57785d8893d8f977807bfb45cac0fc787ccbf58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844472"
---
# <a name="wm_get_license_data-structure"></a>WM \_ 取得 \_ 授權 \_ 資料結構

**WM \_ 取得 \_ 授權 \_ 資料** 結構包含取得 [*DRM*](wmformat-glossary.md) [*授權*](wmformat-glossary.md)之位置的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _WMGetLicenseData {
  DWORD   dwSize;
  HRESULT hr;
  WCHAR   *wszURL;
  WCHAR   *wszLocalFilename;
  BYTE    *pbPostData;
  DWORD   dwPostDataSize;
} WM_GET_LICENSE_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**dwSize**
</dt> <dd>

**DWORD** ，包含 **WM \_ 取得 \_ 授權 \_ 資料** 結構的大小（以位元組為單位）。

</dd> <dt>

**小時**
</dt> <dd>

**HRESULT** 傳回碼。

</dd> <dt>

**wszURL**
</dt> <dd>

寬字元以 null 終止的字串，其中包含授權取得 URL。 在非無訊息授權取得中使用此字串和 **pbPostData** 字串。

</dd> <dt>

**wszLocalFilename**
</dt> <dd>

寬字元以 null 終止的字串，其中包含由 DRM 元件產生的本機 HTML 網頁。 當此字串載入至瀏覽器時，它會自動將 HTTP 要求重新導向至授權取得 URL，以及必要的 post 資料。 此本機 URL 的使用現在已被取代。 建議的方法是使用 **wszURL** 和 **pbPostData** 字串。

</dd> <dt>

**pbPostData**
</dt> <dd>

位元組陣列的指標，其中包含要張貼到授權取得 URL 的資料。 您必須將下列字串加入至 **pbPostData** 字串的開頭： "nonsilent = 1&挑戰 ="。 當您形成 HTTP 要求時，結果字串應該附加至 **wszURL** 。

</dd> <dt>

**dwPostDataSize**
</dt> <dd>

**DWORD** ，指出 **pbPostData** 中未包含 "nonsilent = 1&挑戰 =" 字串的 **pbPostData** 大小。

</dd> </dl>

## <a name="remarks"></a>備註

如果 **WMT \_ 狀態** 等於 **WMT \_ 沒有任何 \_ 許可權（ \_ 例如** 或 **WMT \_ 取得 \_ 授權**），則會在 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)方法的 *pValue* 參數中傳回這個填入的結構。 針對 WMT \_ 沒有任何 \_ 許可權的 \_ EX 事件， **hr** 成員將會是 NS \_ e \_ license \_ REQUIRED、ns \_ e \_ license \_ 過期或 ns \_ e \_ 授權 \_ 不正確的 \_ 許可權。 任何這些錯誤都表示必須藉由流覽至 **wszURL** 成員中的 URL 來取得新的授權。

針對 WMT \_ 取得 \_ 授權事件，如果成功取得授權， **hr** 成員將會傳遞成功的宏。 如果在嘗試無訊息取得之後收到此事件，且 **hr** 等於 NS \_ E \_ DRM \_ 授權 \_ NOTACQUIRED，則表示此授權的授權伺服器僅支援非無訊息的取得。

>audioplayer 範例應用程式會示範如何正確地使用此結構中傳回的資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                      |
| 版本<br/>                  | WindowsMedia Format 7 SDK 或更新版本的 SDK<br/>                       |
| 標頭<br/>                   | <dl> <dt>Drmexternals。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMReader：： AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense)
</dt> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 





