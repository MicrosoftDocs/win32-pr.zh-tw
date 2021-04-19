---
description: 部署以加快通訊速度
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: 部署以加快通訊速度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2594a7dbd34813013257350e2deb9d93db6bae5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972797"
---
# <a name="deploying-for-faster-communication"></a>部署以加快通訊速度

在部署 COM + 應用程式時，效能是一個重要的考慮，而元件位置是從設計完善的應用程式取得最佳效能的關鍵。

只要將應用程式的主要元件移到更快的硬體，就可以解決效能問題。 這已證明不成立。 效能問題不是來自個別元件效能，而是從連接元件的連結所引發。

成功的主要因素是位置。 鄰近性或實體位置、時間、容量和用途是適用于 COM + 應用程式部署之位置的不同層面，全都會影響效能。

當應用程式元件和資源經過設計和部署，以符合應用程式工作負載所放置的需求時，效能最佳。

一般而言，您應該部署元件以將跨進程（尤其是跨電腦）元件之間的通訊降至最低。 如果您的應用程式設計很有效率，元件內的類別會使用和函式進行分組，以最大化元件內的通訊。 在部署元件中，您必須確保元件在邏輯上會使用元件之間的關聯性，並減少元件之間的訊息量。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設計部署](designing-for-deployment.md)
</dt> </dl>

 

 



