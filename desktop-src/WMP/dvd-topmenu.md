---
title: TopMenu 方法
description: TopMenu 方法會停止播放標題，並顯示目前標題的上方 (或根) 功能表。
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- topMenu 方法 Windows Media Player
- topMenu 方法 Windows Media Player、DVD 類別
- DVD 類別 Windows Media Player，topMenu 方法
topic_type:
- apiref
api_name:
- DVD.topMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be2b0fdafb10039b24f1d77e65f4b105889da85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465749"
---
# <a name="dvdtopmenu-method"></a>TopMenu 方法

**TopMenu** 方法會停止播放標題，並顯示目前標題的上方 (或根) 功能表。

## <a name="syntax"></a>語法


```JScript
DVD.topMenu()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

每個 DVD 的撰寫方式不同。 DVD 必須包含功能表，這個方法才能運作。 撰寫一些 Dvd，讓 **topMenu** 和 **titleMenu** 方法開啟相同的功能表。 **TopMenu** 方法通常會叫用 top (或 root) 功能表，但如果沒有可用的根功能表，它可能會改為叫用標題功能表。

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
</dt> <dt>

[**TitleMenu**](dvd-titlemenu.md)
</dt> </dl>

 

 





