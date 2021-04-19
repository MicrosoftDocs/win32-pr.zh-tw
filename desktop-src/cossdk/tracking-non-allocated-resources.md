---
description: 追蹤未配置的資源
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: 追蹤未配置的資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c9f814e08798b4fbb0f160e0d0e0f8aabebba7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984153"
---
# <a name="tracking-non-allocated-resources"></a>追蹤未配置的資源

根據物件的存留期知識，分配者管理員可以追蹤未清查的資源。 當追蹤的非配置資源釋出時，它會被終結，因此不會傳回給清查。 這項僅限追蹤模式適用于不需要建立和終結的資源，比將這些資源儲存在清查中更為實用。 這種模式也適用于管理記憶體分配程式，或針對難以清查的資源，因為有太多不同的類型。

在僅限追蹤模式中，資源配置器會直接建立要求的資源，而不是要求分配者管理員從清查配置一個。 在將此資源傳回給提出要求的應用程式元件之前，資源配置器會告知分配者管理員追蹤資源，這可確保即使元件在忘了釋出資源，當元件的存留期結束時，分配器管理員也會這麼做。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 資源配置器概念](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



