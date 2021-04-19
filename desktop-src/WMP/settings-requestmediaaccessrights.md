---
title: RequestMediaAccessRights 方法
description: RequestMediaAccessRights 方法會要求存取程式庫的指定層級。 |RequestMediaAccessRights 方法
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- requestMediaAccessRights 方法 Windows Media Player
- requestMediaAccessRights 方法 Windows Media Player，Settings 類別
- Settings 類別 Windows Media Player，requestMediaAccessRights 方法
topic_type:
- apiref
api_name:
- Settings.requestMediaAccessRights
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfeed45666ee1f63bf995b211030b0b840c4279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994262"
---
# <a name="settingsrequestmediaaccessrights-method"></a>RequestMediaAccessRights 方法

**RequestMediaAccessRights** 方法會要求存取程式庫的指定層級。

## <a name="syntax"></a>語法


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*存取* \[在\]
</dt> <dd>

**字串** ，指定所需的存取權限層級。 包含下列其中一個值。



| String | Description                      |
|--------|----------------------------------|
| 無   | 僅限目前的專案存取權限。 |
| 讀取   | 僅限讀取存取許可權。         |
| 完整   | 讀取/寫入存取權限。        |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **布林** 值，指出是否已授與要求的存取權限。

## <a name="remarks"></a>備註

網頁必須先向使用者要求許可權，以讀取或寫入文件庫中的資料。 叫用這個方法會提示使用者一個對話方塊，要求指定的許可權等級。 這表示，如果未授與適當的存取權限，就無法從程式碼存取某些方法、屬性和事件。 您可以使用 *設定* 來抓取目前的存取權限層級。**mediaAccessRights**。

**Windows Media Player 10** 行動裝置版：此方法一律會傳回 **true**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Settings 物件**](settings-object.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> </dl>

 

 





