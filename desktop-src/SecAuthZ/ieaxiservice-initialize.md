---
description: 檢查和下載 ActiveX 物件。
ms.assetid: a477c6dc-32a7-4d17-a997-6df4967d6c55
title: IeAxiService：： Initialize 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Initialize
api_type:
- COM
api_location: ''
ms.openlocfilehash: 911d955f84d81b225a1b4062e47b2b9b6ab6d058aa6df2e6a72a8d40242345a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414888"
---
# <a name="ieaxiserviceinitialize-method"></a>IeAxiService：： Initialize 方法

**Initialize** 方法會檢查並下載 ActiveX 物件。 如果物件符合原則需求，這個方法會初始化安裝 ActiveX 物件的系統物件。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS Initialize(
  [in]  HWND     hwndParent,
  [in]  DWORD    dwClientPID,
  [in]  BSTR     bstrDesktop,
  [in]  BSTR     bstrClsID,
  [in]  BSTR     bstrURL,
  [out] BSTR     *pbstrNonce,
  [out] IUnknown **ppISyncBrokerInterface
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndParent* \[在\]
</dt> <dd>

嘗試安裝 ActiveX 控制項之視窗的父視窗的控制碼。

</dd> <dt>

*dwClientPID* \[在\]
</dt> <dd>

呼叫進程的處理序識別碼。

</dd> <dt>

*bstrDesktop* \[在\]
</dt> <dd>

物件的桌面。

</dd> <dt>

*bstrClsID* \[在\]
</dt> <dd>

要安裝之 ActiveX 物件的類別識別碼。

</dd> <dt>

*bstrURL* \[在\]
</dt> <dd>

要安裝之 ActiveX 物件的 URL。

</dd> <dt>

*pbstrNonce* \[擴展\]
</dt> <dd>

可以用來在呼叫其他方法時，用來共用狀態資訊的內容，用來驗證和下載 ActiveX 物件。

</dd> <dt>

*ppISyncBrokerInterface* \[擴展\]
</dt> <dd>

[**IeAxiSystemInstaller**](ieaxisysteminstaller.md)介面實例的指標，該實例會安裝 ActiveX 控制項。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 S \_ OK。

如果函式失敗，則傳回值可以是下列其中一個錯誤碼。



| 傳回碼/值                                                                                                                                                              | Description                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**信任 \_電子 \_ 主體 \_ 不 \_ 受信任**</dt> <dt>0x800B0004</dt> </dl> | 不應安裝 ActiveX 物件。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windowsvista Business、Windows vista Enterprise、Windows vista 旗艦版傳統型 \[ 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService 定義為 E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IeAxiService**](ieaxiservice.md)
</dt> </dl>

 

 




