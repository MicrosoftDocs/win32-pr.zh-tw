---
title: 設定. mediaAccessRights
description: MediaAccessRights 屬性會取得值，指出目前授與存取程式庫的許可權。
ms.assetid: 744e696d-29d2-44b1-a296-5b5d007b689f
keywords:
- 設定的 mediaAccessRights Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mediaAccessRights
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b78543adcdc36958c6fb2f8e4ea191156bd8c600112e4bd6e5d6e6f5427974
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117933658"
---
# <a name="settingsmediaaccessrights"></a>設定. mediaAccessRights

**MediaAccessRights** 屬性會取得值，指出目前授與存取程式庫的許可權。

## <a name="syntax"></a>Syntax

mediaAccessRights

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串**。



| 值 | 描述                      |
|-------|----------------------------------|
| 無  | 僅限目前的專案存取權限。 |
| 讀取  | 僅限讀取存取許可權。         |
| 完整  | 讀取/寫入存取權限。        |



 

## <a name="remarks"></a>備註

網頁必須先向使用者要求許可權，以讀取或寫入文件庫中的資料。 這表示，如果未授與適當的存取權限，就無法從程式碼存取某些方法、屬性和事件。 為了取得存取權限，應用程式會呼叫 *設定*。**requestMediaAccessRights**，傳遞指定所需存取權限層級的參數。

**Windows Media Player 10** 行動裝置版：此屬性一律會傳回 **full**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**設定物件**](settings-object.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





