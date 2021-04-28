---
description: IWiaUIExtension：： GetDeviceIcon 方法-取得自訂裝置圖示。
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: 'IWiaUIExtension：： GetDeviceIcon 方法 (Wiadevd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 9bfa8e87736412822c1a70f75b129aeec30af20e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116656"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a>IWiaUIExtension：： GetDeviceIcon 方法

取得自訂裝置圖示。

## <a name="syntax"></a>語法


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrDeviceId* \[在\]
</dt> <dd>

類型： **BSTR**

指定要取得其圖示之 WIA 裝置的裝置識別碼。

</dd> <dt>

*phIcon* \[擴展\]
</dt> <dd>

類型： **HICON \***

指向將接收裝置圖示控制碼的記憶體位置。

</dd> <dt>

*nSize* \[在\]
</dt> <dd>

類型： **ULONG**

指定所需的圖示大小（以圖元為單位）。 此圖示會假設為正方形，而 nSize 會指定所要求圖示的寬度和高度。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wiadevd。h</dt> </dl> |



 

 




