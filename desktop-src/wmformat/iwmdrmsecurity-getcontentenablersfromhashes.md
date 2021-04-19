---
title: 'IWMDRMSecurity GetContentEnablersFromHashes 方法 (Wmdrmsdk .h) '
description: GetContentEnablersFromHashes 方法會抓取內容啟用程式介面，以根據已雜湊的憑證來更新元件。
ms.assetid: d7429859-b609-49a2-a369-d02260bc15bf
keywords:
- GetContentEnablersFromHashes 方法 windows Media 格式
- GetContentEnablersFromHashes 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，GetContentEnablersFromHashes 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersFromHashes
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44b4187699cb4a55d0c6215e3f31b430a87d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983981"
---
# <a name="iwmdrmsecuritygetcontentenablersfromhashes-method"></a>IWMDRMSecurity：： GetContentEnablersFromHashes 方法

**GetContentEnablersFromHashes** 方法會抓取內容啟用程式介面，以根據已雜湊的憑證來更新元件。

## <a name="syntax"></a>語法


```C++
HRESULT GetContentEnablersFromHashes(
  [in]      BSTR              *rgpbCertHashes,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rgpbCertHashes* \[在\]
</dt> <dd>

憑證雜湊的陣列，用來取得的內容啟用程式。

</dd> <dt>

*cCerts* \[在\]
</dt> <dd>

要取出內容啟用程式的憑證數目。 這是 *rgpbCertHashes* 陣列中的元素數目。

</dd> <dt>

*hResultHint* \[在\]
</dt> <dd>

因為撤銷憑證而失敗的作業所收到的傳回值。 如果您未呼叫來回應失敗的方法呼叫，請將設定為 \_ [確定]。

</dd> <dt>

*prgContentEnablers* \[擴展\]
</dt> <dd>

接收新建立之 **IMFContentEnabler** 介面位址的陣列。 設定為 **Null** ，以取得 *pcContentEnablers* 參數中的內容啟用程式數目。

</dd> <dt>

*pcContentEnablers* \[in、out\]
</dt> <dd>

*PrgContentEnablers* 陣列中的元素數目。 如果 *prgContentEnablers* 為 **Null**，則此值會設定為輸出上所需的內容啟用程式數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

如果您使用 **IMFContentEnabler** 介面更新撤銷的元件，您必須明確地說明使用者的流程。 因為更新程式會將用戶端電腦的資訊傳送到 Microsoft 網站，所以必須進行這種澄清。

當您呼叫 **IMFContentEnabler：： AutomaticEnable** 時，內容啟用程式會以 Microsoft 網站上的更新服務位址啟動預設的瀏覽器。 識別已撤銷元件的唯一識別碼會傳送至 update 服務。 接著，服務會將瀏覽器重新導向至網頁，讓使用者可以從該網頁下載並安裝新的已撤銷元件版本。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMSecurity 介面**](iwmdrmsecurity.md)
</dt> </dl>

 

 





