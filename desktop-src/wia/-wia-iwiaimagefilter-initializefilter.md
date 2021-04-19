---
description: 初始化篩選。 在每個映射下載之前，Windows 映像取得 (WIA) 2.0 中呼叫。
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: 'IWiaImageFilter：： InitializeFilter 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.InitializeFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a113c9493128a634ce61ccf7c0362bf7a9767f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974689"
---
# <a name="iwiaimagefilterinitializefilter-method"></a>IWiaImageFilter：： InitializeFilter 方法

初始化篩選。 在每個映射下載之前，Windows 映像取得 (WIA) 2.0 中呼叫。

## <a name="syntax"></a>語法


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pWiaItem2* \[在\]
</dt> <dd>

類型： **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

指定代表預覽影像之 [_ *IWiaItem2* *](-wia-iwiaitem2.md)專案的指標。

</dd> <dt>

*pWiaTransferCallback* \[在\]
</dt> <dd>

類型： **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _

指定應用程式 [_ *IWiaTransferCallback* *](-wia-iwiatransfercallback.md)介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

當應用程式呼叫「 [**下載**](-wia-iwiatransfer-download.md) 」時，以及當應用程式呼叫 WIA 2.0 Preview 元件的函式時，會呼叫這個方法 `GetNewPreview` 。 **IWiaImageFilter：： InitializeFilter** 會儲存 *pWiaItem2* 和 *pWiaTransferCallback* 的參考，以傳遞至這些函數。 這兩個介面指標應儲存為成員變數，且應該為每個介面呼叫 [IUnknown：： AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 。 在取得映射期間， [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) 和 [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) 的篩選器執行中也需要介面指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
