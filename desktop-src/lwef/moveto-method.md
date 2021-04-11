---
title: MoveTo 方法
description: MoveTo 方法
ms.assetid: cca2b1b8-0d44-4272-9f0b-f7afd091d802
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6a7f215de9ea6e323870ec7e10967462ab4174
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023477"
---
# <a name="moveto-method"></a>MoveTo 方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

將指定的字元移動至指定的位置。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "*** CharacterID * * *" 的字元 ) 。MoveTo* *  *x、y* \[ *速度*\]



| 部分    | 描述                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x、y*   | 必要。 整數值，指出動畫框架的左邊緣 (*x*) 和上邊緣 (*y*) 。 表示這些座標（以圖元為單位）。                                                   |
| *速度* | 選擇性。 長整數值，以毫秒為單位，指定字元畫面格移動的速度。 預設值為 1000。 指定零 (0) 移動框架，而不播放動畫。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

伺服器會自動播放指派給 **移動** 狀態的適當動畫。 字元的位置是根據其框架的左上角。

如果您宣告物件變數，並將它設定為此方法，則會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。 此外，如果尚未在本機電腦上載入相關聯的動畫，伺服器會將 **要求** 物件的 [ [**狀態**](status-property.md) ] 屬性設定為 [失敗]，並提供適當的錯誤號碼。 因此，如果您使用 HTTP 通訊協定來存取字元或動畫資料，請使用 [**Get**](get-method.md) 方法來載入 **移動** 狀態動畫，然後再呼叫 **MoveTo** 方法。

即使未載入動畫，伺服器還是會移動框架。

> [!Note]  
> 如果您在顯示該字元之前，使用非零值來呼叫 **MoveTo** ，則會傳回失敗狀態，因為非零 [](/windows/desktop/lwef/the-request-object)值表示您嘗試在不顯示該字元時播放動畫。

 

> [!Note]  
> *速度* 參數的實際效果可能會根據電腦處理器的速度，以及系統上執行之其他工作的優先順序而有所不同。

 

 

 