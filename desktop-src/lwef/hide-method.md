---
title: Hide 方法
description: Hide 方法
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67057464c8e505e56123f712d3a1e6d668c7d75b00bc4732e7b18195b3be9723
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725448"
---
# <a name="hide-method"></a>Hide 方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

隱藏指定的字元。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。隱藏_ *  \[ *快速*\]



| 部分   | 描述                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *快速* | 選擇性。 布林值，指出是否略過與字元隱藏狀態 **True** 相關聯的動畫不播放 **隱藏** 動畫。 <br/> **False** (預設) 播放 **隱藏** 動畫。 <br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

伺服器會在字元的佇列中將 **Hide** 方法的動作排入佇列，讓您可以使用它來隱藏其他動畫序列之後的字元。 您可以在呼叫這個方法之前，使用 [**Stop**](stop-method.md) 方法立即播放動作。

如果您宣告物件參考，並將它設定為此方法，則會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。 此外，如果關聯的 **隱藏** 動畫尚未載入，而且您尚未將 **Fast** 參數指定為 **True**，則伺服器會將 [ **要求** 物件 [**狀態**](status-property.md) ] 屬性設定為 [失敗]，並提供適當的錯誤號碼。 因此，如果您使用 HTTP 通訊協定來存取字元或動畫資料，請使用 [**Get**](get-method.md)方法，並在呼叫 **Hide** 方法之前，指定要載入動畫的 **隱藏** 狀態。

隱藏字元也可能導致觸發另一個用戶端的 [**ActivateInput**](activateinput-event.md) 事件。

> [!Note]  
> 隱藏的字元無法存取音訊通道。 如果您產生動畫要求且隱藏字元，伺服器將會在 [**RequestComplete**](requestcomplete-event.md) 事件中傳回失敗狀態。

 

## <a name="see-also"></a>另請參閱

[**Show 方法**](show-method.md)


 

