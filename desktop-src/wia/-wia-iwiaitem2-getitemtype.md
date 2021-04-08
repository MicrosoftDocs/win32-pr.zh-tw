---
description: 取得專案的類型資訊。
ms.assetid: 9670f184-e8ba-4596-af6d-2967320dfd95
title: 'IWiaItem2：： GetItemType 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemType
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3bf177ddcc117cdfe21a1b9322a0e457cf899c0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690568"
---
# <a name="iwiaitem2getitemtype-method"></a>IWiaItem2：： GetItemType 方法

取得專案的類型資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetItemType(
  [out] LONG *pItemType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pItemType* \[擴展\]
</dt> <dd>

類型： **LONG \** _

接收 _ *LONG** 的指標，其中包含類型旗標的組合。 請參閱 [**WIA 專案類型旗標**](-wia-wia-item-type-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

與 Windows 映像取得相關聯之物件的階層式樹狀結構中的每個 [**IWiaItem2**](-wia-iwiaitem2.md) 物件 (WIA) 2.0 硬體裝置都有特定的資料類型。 專案物件代表資料夾和檔案。 資料夾包含檔案物件。 檔案物件包含裝置所取得的資料，例如影像和聲音。 這個方法可讓應用程式在裝置的專案物件階層式樹狀結構中，識別任何專案的型別。

一個專案可以有一個以上的類型。 例如，代表音訊檔案的專案將會有 type 屬性 [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 




