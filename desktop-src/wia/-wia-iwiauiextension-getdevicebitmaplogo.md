---
description: 取得裝置的自訂點陣圖標誌。
ms.assetid: 56b3c7c9-64f4-4853-9eb7-d876d02a851f
title: 'IWiaUIExtension：： GetDeviceBitmapLogo 方法 (Wiadevd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceBitmapLogo
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 057216a3b482abae564126cf0bf74198b24fab279c3faf3aa02dedad8fb65a30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118034966"
---
# <a name="iwiauiextensiongetdevicebitmaplogo-method"></a>IWiaUIExtension：： GetDeviceBitmapLogo 方法

取得裝置的自訂點陣圖標誌。

## <a name="syntax"></a>語法


```C++
HRESULT GetDeviceBitmapLogo(
  [in]  BSTR    bstrDeviceId,
  [out] HBITMAP *phBitmap,
  [in]  ULONG   nMaxWidth,
  [in]  ULONG   nMaxHeight
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrDeviceId* \[在\]
</dt> <dd>

類型： **BSTR**

指定要取得其圖示之 WIA 裝置的裝置識別碼。

</dd> <dt>

*phBitmap* \[擴展\]
</dt> <dd>

類型： **HBITMAP \***

指向將接收裝置點陣圖標誌之控制碼的記憶體位置。

</dd> <dt>

*nMaxWidth* \[在\]
</dt> <dd>

類型： **ULONG**

指定點陣圖所需的寬度。

</dd> <dt>

*nMaxHeight* \[在\]
</dt> <dd>

類型： **ULONG**

指定所需的點陣圖高度。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wiadevd。h</dt> </dl> |



 

 




