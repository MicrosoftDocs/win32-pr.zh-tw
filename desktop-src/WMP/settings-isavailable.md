---
title: 設定. isAvailable
description: IsAvailable 屬性會指出是否可以使用指定的資訊類型，或可以執行指定的動作。 |設定. isAvailable
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- 設定的 isAvailable Windows Media Player
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
ms.openlocfilehash: df10026007dd9e04fe88d634a3da566074b0d6a88420ef444d5f2bae39a793fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002408"
---
# <a name="settingsisavailable"></a>設定. isAvailable

**IsAvailable** 屬性會指出是否可以使用指定的資訊類型，或可以執行指定的動作。

## <a name="syntax"></a>Syntax

isAvailable ( 名稱 ) 

## <a name="parameters"></a>參數

*name*

包含下列其中一個值的字串。



| String             | 描述                                                    |
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

[**設定物件**](settings-object.md)
</dt> </dl>

 

 





