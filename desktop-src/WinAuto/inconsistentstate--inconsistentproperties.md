---
title: InconsistentState, InconsistentProperties
description: InconsistentState, InconsistentProperties
ms.assetid: 82A2ECA8-0155-402A-A745-B97D3F633643
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5522025eff8aecbdf0f4313c0052afebd4a17958
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672019"
---
# <a name="inconsistentstate-inconsistentproperties"></a>InconsistentState, InconsistentProperties

## <a name="text"></a>Text

控制項具有不一致的狀態/屬性 {0}{1}

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

元素報告不一致或衝突的 MSAA 狀態或消費者介面自動化屬性。 例如，當 [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) 方法傳回下列任何組合時。

-   狀態 \_ 系統已 \_ 展開且狀態 \_ 系統 \_ 已折迭
-   已 \_ 選取狀態系統 \_ ，但無法選取狀態 \_ 系統 \_
-   以狀態 \_ 系統為 \_ 焦點且不是狀態 \_ 系統可 \_ 設定焦點

這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員遇到問題，因為可能會向使用者回報不正確的元素狀態。

## <a name="possible-causes"></a>可能的原因

元素或其父系的 MSAA 狀態設定不當。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IAccessible：： get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**物件狀態常數**](object-state-constants.md)
</dt> <dt>

[狀態和屬性](uiauto-msaa.md)
</dt> </dl>

 

 




