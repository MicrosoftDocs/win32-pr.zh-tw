---
title: Active Accessibility 和消費者介面自動化
description: Microsoft Active Accessibility 是專為搭配 Windows XP 和舊版作業系統使用所設計。
ms.assetid: 8eb36d2c-0c2f-4311-8690-52ce070c9f33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2483f4f6679926ef2f87c380d4ac0febcc88652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966414"
---
# <a name="active-accessibility-and-ui-automation"></a>Active Accessibility 和消費者介面自動化

Microsoft Active Accessibility 是專為搭配 Windows XP 和舊版作業系統使用所設計。 適用于 Windows XP 和 Windows Vista 的自訂控制項和可存取技術用戶端應用程式的開發人員，應該考慮改為使用 Microsoft [消費者介面自動化](entry-uiauto-win32.md) 。

Microsoft 消費者介面自動化是一種功能完整的系統，可提供更精確的使用者介面相關資訊，並讓使用者更能夠與控制項互動。 尤其是，它提供大幅增強的文字支援。

一組 proxy 物件提供標準 Microsoft Win32 和 Windows Forms 控制項的消費者介面自動化支援。 更豐富的支援適用于特別以消費者介面自動化撰寫的控制項，包括原生 Windows Presentation Foundation (WPF) 元素，這些專案不會直接支援 Microsoft Active Accessibility。 支援消費者介面自動化的自訂控制項可以撰寫為 managed 或非受控碼。

Microsoft Active Accessibility 的用戶端會透過橋接層存取有限的 UI 元素，僅支援消費者介面自動化。 如需詳細資訊，請參閱 [附錄 G： Active Accessibility 橋接器至消費者介面自動化](appendix-g--active-accessibility-bridge-to-ui-automation.md)。

如需有關 Microsoft Active Accessibility 和消費者介面自動化之間的相似性和差異的詳細資訊，請參閱 [Microsoft Active Accessibility 和消費者介面自動化比較](microsoft-active-accessibility-and-ui-automation-compared.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[快速入門](getting-started.md)
</dt> <dt>

[使用者介面自動化](entry-uiauto-win32.md)
</dt> </dl>

 

 




