---
title: 設定. isAvailable
description: IsAvailable 屬性會指出是否可以使用指定的資訊類型，或可以執行指定的動作。 |設定. isAvailable
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- 設定. isAvailable Windows Media Player
topic_type:
- apiref
api_name:
- Settings.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96923fa57ffab4fb2e47b16afd03a06bbffd0ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992895"
---
# <a name="settingsisavailable"></a>設定. isAvailable

**IsAvailable** 屬性會指出是否可以使用指定的資訊類型，或可以執行指定的動作。

## <a name="syntax"></a>Syntax

isAvailable ( 名稱 ) 

## <a name="parameters"></a>參數

*name*

包含下列其中一個值的字串。



| String             | Description                                                    |
|--------------------|----------------------------------------------------------------|
| AutoStart          | 判斷是否可以設定自動啟動屬性。          |
| 餘額            | 決定是否可以設定餘額屬性。            |
| BaseURL            | 判斷是否可以設定 baseURL 屬性。            |
| DefaultFrame       | 判斷是否可以設定 defaultFrame 屬性。       |
| EnableErrorDialogs | 判斷是否可以設定 enableErrorDialogs 屬性。 |
| GetMode            | 判斷是否可以呼叫 getMode 方法。           |
| InvokeURLs         | 判斷是否可以設定 invokeURLs 屬性。         |
| Mute               | 決定是否可以設定靜音屬性。               |
| PlayCount          | 判斷是否可以設定 playCount 屬性。          |
| 費率               | 決定是否可以設定速率屬性。               |
| SetMode            | 判斷是否可以呼叫 setMode 方法。           |
| 磁碟區             | 判斷是否可以設定磁片區屬性。             |



 

## <a name="return-values"></a>傳回值

這個方法會傳回 **布林** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Settings 物件**](settings-object.md)
</dt> </dl>

 

 





