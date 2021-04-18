---
title: NDF helper 類別延伸的 UI 指導方針
description: 建立協助程式類別時，您將需要建立文字，以協助使用者瞭解事件的原因，以及可採取的可能修復步驟。
ms.assetid: f13f3621-ab82-4e22-9442-0a4d57c368fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e48357ba6561ab135e2c341409c22d1edf3fb7d
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/12/2019
ms.locfileid: "104313586"
---
# <a name="ui-guidelines-for-ndf-helper-class-extensions"></a>NDF helper 類別延伸的 UI 指導方針

建立協助程式類別時，您將需要建立文字，以協助使用者瞭解事件的原因，以及可採取的可能修復步驟。

## <a name="root-cause-and-repair"></a>根本原因和修復

發生事件時，會出現一個對話方塊，告知使用者發生了什麼事。 您所建立的文字將會出現在兩個不同的區域中。

-   **根本原因**：問題原因的簡短描述。 包含可協助系統管理員或 advanced 使用者針對問題進行疑難排解的資訊。
-   **修復**：展開根本原因，以提供使用者可採取之步驟的詳細資料，而不會變得太長。

每個根本原因或修復都應該有標題和描述。 第一個 "n" 字元之前的所有文字 \\ 將會用於標題。 前 "n" 個字元後面的所有文字 \\ (包括任何後續分行符號) 將用於描述。

## <a name="title-guidelines"></a>標題指導方針

根本原因或修復的標題應該遵循下列指導方針：

-   必須為128個字元或更少。 建議 (40 個字元或更少。 ) 
-   不應以句號結尾。

## <a name="description-guidelines"></a>描述方針

根本原因或修復的描述應遵循下列指導方針：

-   必須為512個字元或更少。
-   每個句子的結尾都應該是句號。
-   " \\ N" 字元可以用來在描述中建立分行符號。

 

 




