---
description: 取得專案的類別目錄資訊。
ms.assetid: 4d6f7a6a-280d-4b36-8e1d-8d9fcaa8a1de
title: 'IWiaItem2：： GetItemCategory 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemCategory
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: fdf650e8b540fcb9dc58f93f34771462fbc0a5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971012"
---
# <a name="iwiaitem2getitemcategory-method"></a>IWiaItem2：： GetItemCategory 方法

取得專案的類別目錄資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetItemCategory(
  [out] GUID *pItemCategoryGUID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pItemCategoryGUID* \[擴展\]
</dt> <dd>

類型： **GUID \** _

接收識別專案類別之 GUID 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： _ *HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

與 Windows 映像取得相關聯之物件的階層式樹狀結構中的每個 [**IWiaItem2**](-wia-iwiaitem2.md) 物件 (WIA) 2.0 硬體裝置都有特定的類別。 此方法可讓應用程式識別裝置中專案物件階層式樹狀結構中任何專案的類別。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 




