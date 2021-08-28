---
description: 從裝置的物件樹狀結構中移除目前的 IWiaItem2 物件。
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: 'IWiaItem2：:D eleteItem 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeleteItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 791d596ee48c4d3e2efd67259ec2e37249c930c6da32f704d332df1da6930503
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592998"
---
# <a name="iwiaitem2deleteitem-method"></a>IWiaItem2：:D eleteItem 方法

從裝置的物件樹狀結構中移除目前的 [**IWiaItem2**](-wia-iwiaitem2.md) 物件。

## <a name="syntax"></a>語法


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

目前未使用。 應該設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

Windows 的影像取得 (WIA) 2.0 執行時間系統會將連接到使用者電腦的每個 WIA 2.0 硬體裝置，表示為 [**IWiaItem2**](-wia-iwiaitem2.md)物件的階層式樹狀結構。 指定的 WIA 2.0 裝置不一定會允許應用程式從其樹狀結構中刪除 **IWiaItem2** 物件。 無法刪除具有子系的專案。 [**IEnumWIA \_ DEV \_ cap**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)介面必須用來查詢裝置以取得專案刪除功能。

如果裝置支援在其 [**IWiaItem2**](-wia-iwiaitem2.md) 樹狀目錄中刪除專案，請呼叫 **IWiaItem2：:D eleteitem** 方法以移除 **IWiaItem2** 物件。 請注意，這個方法只會在對物件的所有參考都已釋放之後刪除物件。 如果專案的刪除失敗， \_ 則會傳回 E DELETEITEM。 尚未定義此錯誤的數值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 




