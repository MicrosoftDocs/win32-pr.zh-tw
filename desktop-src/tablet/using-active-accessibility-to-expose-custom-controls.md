---
description: 使用主動式存取範圍來公開 Tablet PC 自訂控制項的描述。
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: 使用 Active Accessibility 來公開自訂控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d275b6c5639dddfe60f358427751ad4ff4cd7989923dc4a368b3316b3bfc01e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934318"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a>使用 Active Accessibility 來公開自訂控制項

您可以使用 Microsoft Active Accessibility 作為讓自訂控制項與協助工具輔助相容的有效方式。 Active Accessibility 需要應用程式：

-   建立元件物件模型 (COM) 物件，這些物件代表個別的自訂控制項或正確支援 **IAccessible** 介面的控制項群組。  (當 Active Accessibility 用戶端要求物件時，可能會視需要建立物件。 ) 
-   當控制項建立或損毀、獲得或失去焦點，或變更狀態時，呼叫 [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) 。
-   \_用來查詢物件或物件的屬性時，處理 WM GETOBJECT 訊息。

基於本文的目的，也需要公開一個包含其他自訂物件的視窗來 Active Accessibility，讓用戶端可以探索並流覽至子物件。 如需如何使自訂控制項與協助工具協助工具相容的詳細資訊，請參閱 [協助工具](../accessibility/accessibility.md)。

 

 
