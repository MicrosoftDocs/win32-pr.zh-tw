---
description: DEP/NX 保護
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: DEP/NX 保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec30b3758361cbe2ed20e67fe6792d6f76b58a7266c6de1d554afdba8a2519c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329938"
---
# <a name="depnx-protection"></a>DEP/NX 保護

從 Windows Vista 上的 Windows Internet Explorer 7 開始，[網際網路控制台] 專案包含 [**啟用記憶體保護**] 選項，可協助您減輕線上攻擊的風險。 此選項也稱為「 *資料執行防護* 」 (DEP) 或「 *不執行* 」 (NX) 。 啟用此選項時，它會與處理器搭配運作，藉由封鎖標記為無法執行的記憶體中的程式碼執行，以協助防止緩衝區溢位攻擊。

在 Windows Internet Explorer 8 Windows Vista Service Pack 1 (SP1) 作業系統或更新版本上，預設會啟用此選項。 DEP/NX 無法防止所有以記憶體為基礎的弱點。 但是，當它與其他技術（例如位址空間配置隨機載入）結合 (ASLR) 時，它有助於防止 Windows Internet Explorer 中常見的緩衝區溢位弱點，以及它所載入的附加元件。 不需要額外的使用者互動來提供此保護，也不會引進任何新的提示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用相容性檢視修正 Web 應用程式中的相容性問題](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



