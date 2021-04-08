---
description: 取得專案物件樹狀結構的根專案，用來表示 Windows 映像取得 (WIA) 2.0 硬體裝置。
ms.assetid: bc31ad4a-0851-4510-a038-83646ffd5c98
title: 'IWiaItem2：： GetRootItem 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetRootItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c8d4f004cc9c7cabaf4898f5e8c838a0399dc106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690567"
---
# <a name="iwiaitem2getrootitem-method"></a>IWiaItem2：： GetRootItem 方法

取得專案物件樹狀結構的根專案，用來表示 Windows 映像取得 (WIA) 2.0 硬體裝置。

## <a name="syntax"></a>語法


```C++
HRESULT GetRootItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppIWiaItem2* \[擴展\]
</dt> <dd>

類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

接收根專案之 [**IWiaItem2**](-wia-iwiaitem2.md) 介面指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

針對 WIA 2.0 硬體裝置的物件樹狀結構中的任何 [**IWiaItem2**](-wia-iwiaitem2.md) 物件，應用程式會呼叫這個函式，以抓取根專案的指標。

應用程式必須在透過 *ppIWiaItem2* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
