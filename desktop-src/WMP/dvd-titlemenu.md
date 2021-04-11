---
title: TitleMenu 方法
description: TitleMenu 方法會停止播放標題，並顯示標題功能表。
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- titleMenu 方法 Windows Media Player
- titleMenu 方法 Windows Media Player、DVD 類別
- DVD 類別 Windows Media Player，titleMenu 方法
topic_type:
- apiref
api_name:
- DVD.titleMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9351603d5307415f57610422a83d3586067bdcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317212"
---
# <a name="dvdtitlemenu-method"></a>TitleMenu 方法

**TitleMenu** 方法會停止播放標題，並顯示標題功能表。

## <a name="syntax"></a>語法


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

每個 DVD 的撰寫方式不同。 DVD 必須包含功能表，這個方法才能運作。 撰寫一些 Dvd，讓 **topMenu** 和 **titleMenu** 方法開啟相同的功能表。 **TitleMenu** 方法通常會叫用標題功能表，但如果沒有可用的標題功能表，它可能會叫用上層功能表。

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

[**TopMenu**](dvd-topmenu.md)
</dt> </dl>

 

 





