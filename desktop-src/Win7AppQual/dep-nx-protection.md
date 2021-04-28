---
description: DEP/NX 保護
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: DEP/NX 保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3565460cbfd2e6b13c3c5ba6b1f0693a3d5b25ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088566"
---
# <a name="depnx-protection"></a>DEP/NX 保護

從 windows Vista 上的 Windows Internet Explorer 7 開始，[網際網路控制台] 專案包含了 [ **啟用記憶體保護** ] 選項，可協助減輕線上攻擊的風險。 此選項也稱為「 *資料執行防護* 」 (DEP) 或「 *不執行* 」 (NX) 。 啟用此選項時，它會與處理器搭配運作，藉由封鎖標記為無法執行的記憶體中的程式碼執行，以協助防止緩衝區溢位攻擊。

在 windows Vista （含 Service Pack 1） (SP1) 作業系統或更新版本的 windows Internet Explorer 8 中，預設會啟用此選項。 DEP/NX 無法防止所有以記憶體為基礎的弱點。 但是，當它與其他技術（例如位址空間配置隨機載入）結合 (ASLR) 時，它有助於防止 Windows Internet Explorer 中常見的緩衝區溢位弱點，以及它所載入的增益集。 不需要額外的使用者互動來提供此保護，也不會引進任何新的提示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用相容性檢視修正 Web 應用程式中的相容性問題](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



