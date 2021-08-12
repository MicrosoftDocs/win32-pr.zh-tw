---
description: 提供傳輸期間的進度和其他通知。
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: 'IWiaTransferCallback：： TransferCallback 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.TransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 02c24f4cb1795e233fbbbb3dc30ad1bbb3624e104d59ac72f8e310bbbd323820
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440316"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a>IWiaTransferCallback：： TransferCallback 方法

提供傳輸期間的進度和其他通知。

## <a name="syntax"></a>語法


```C++
HRESULT TransferCallback(
  [in] LONG              lFlags,
  [in] WiaTransferParams *pWiaTransferParams
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

目前未使用。 應該設定為零。

</dd> <dt>

*pWiaTransferParams* \[在\]
</dt> <dd>

類型： **[ **WiaTransferParams**](-wia-wiatransferparams.md)\***

指定 [**WiaTransferParams**](-wia-wiatransferparams.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

當此方法是由影像處理篩選器所執行時，Windows 的影像取得 (WIA) 2.0 迷你驅動程式會在影像取得期間呼叫它，以將進度訊息傳回給應用程式。

篩選準則的 **IWiaTransferCallback：： TransferCallback** 必須委派給應用程式回呼的 **IWiaTransferCallback：： TransferCallback** 方法。 篩選資料流程通常會篩選傳遞給它的資料，並將篩選過的資料直接寫入應用程式提供的資料流程。 當影像處理篩選在其 [IStream：： Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write)方法的呼叫之間儲存資料時，它也必須修改 [**WiaTransferParams**](-wia-wiatransferparams.md)結構中的 *lPercentComplete* 和 *ulBytesWrittenToCurrentStream* 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Wiaguid .lib</dt> </dl> |



 

 
