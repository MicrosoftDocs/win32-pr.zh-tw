---
title: DVD-R 方法
description: Back 方法會將顯示從子功能表傳回至其父功能表。
ms.assetid: 4b6c3562-6484-4ef0-8c5c-c24d88e02096
keywords:
- back 方法 Windows Media Player
- back 方法 Windows Media Player、DVD 類別
- DVD 類別 Windows Media Player、back 方法
topic_type:
- apiref
api_name:
- DVD.back
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e656051d02ec5efc74aa7595d2ca6cb20e648f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384666"
---
# <a name="dvdback-method"></a>DVD-R 方法

Back 方法會將顯示從子功能表 **傳回** 至其父功能表。

## <a name="syntax"></a>語法


```JScript
DVD.back()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

每個 DVD 的撰寫方式不同。 某些 Dvd 的編寫是為了讓 **back** 方法可從根功能表取得，但叫用時，它不會執行任何動作。

**Windows Media Player 10** 行動裝置版：這個方法一律會成功，但不會執行預定的作業。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 版本<br/>                  | 適用于 Windows XP 或更新版本的 Windows Media Player。<br/>                           |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DVD 物件**](dvd-object.md)
</dt> </dl>

 

 





