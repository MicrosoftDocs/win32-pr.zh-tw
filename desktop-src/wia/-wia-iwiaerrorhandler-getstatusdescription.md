---
description: 傳回描述狀態碼的字串。
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: 'IWiaErrorHandler：： GetStatusDescription 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.GetStatusDescription
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: da23e413ee238f43ae577a51b18a542dc1b0768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981436"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a>IWiaErrorHandler：： GetStatusDescription 方法

傳回描述狀態碼的字串。

## <a name="syntax"></a>語法


```C++
HRESULT GetStatusDescription(
  [in]  IUnknown *punkItem,
  [in]  HRESULT  hrStatus,
  [in]  LONG     cbResLength,
  [in]  BYTE     *pbData,
  [out] BSTR     *pbstrDescription
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*punkItem* \[在\]
</dt> <dd>

類型： **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

正在傳送之專案的 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標。 此物件至少會執行 [_ *IWiaItem2* *](-wia-iwiaitem2.md)和 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer)。

</dd> <dt>

*hrStatus* \[在\]
</dt> <dd>

類型： **HRESULT**

**HRESULT** ，這是 [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)所接收的狀態碼。

</dd> <dt>

*cbResLength* \[在\]
</dt> <dd>

類型： **LONG**

**LONG** 是 *>pbdata* 所參考的資料大小。

</dd> <dt>

*>pbdata* \[在\]
</dt> <dd>

類型： **BYTE \** _

[_ *BandedDataCallback* *](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)所接收之資料緩衝區的指標。

</dd> <dt>

*pbstrDescription* \[擴展\]
</dt> <dd>

類型： **BSTR \** _

_ *BSTR** 接收資料傳輸期間發生之狀態或錯誤的描述。 此參數不可以是 **Null**。 呼叫端必須使用 [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)釋放字串，而實作項必須使用 [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring)來配置字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

傳回下列其中一個值。



| 傳回碼                                                                             | Description                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>    | *pbstrDescription* 包含有效的 **BSTR** 指標。 <br/>  |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | *hrStatus* 未知，而且沒有可用的描述。 <br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Wiaguid .lib</dt> </dl> |



 

 
