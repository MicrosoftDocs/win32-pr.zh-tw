---
title: FirstChildLastChildMismatch
description: FirstChildLastChildMismatch
ms.assetid: 98726C1A-DC43-4FC7-8ECA-628F63D0AFE3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37fedb7e23ce2ac2a7f9c51c9db9e06e59ead515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372375"
---
# <a name="firstchildlastchildmismatch"></a>FirstChildLastChildMismatch

## <a name="text"></a>Text

當您 {0} 從已測試的節點進行呼叫，然後重複呼叫時 {1} ，我們已完成下列子系： {2} 。 這不符合在測試的節點上呼叫的結果 {3} ，這會產生： {4} 。 相反地，子系應該報告為測試節點的父代。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

在元素的子系之間流覽時發生問題。 1. 消費者介面自動化的執行不正確或無效。

此問題可能會導致自動化工具的導覽問題，因為進行中的元素可能不穩定且無法預測。

## <a name="possible-causes"></a>可能的原因

消費者介面自動化的執行不正確或無效。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IUIAutomationElement::GetCachedParent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent)
</dt> <dt>

[**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)
</dt> </dl>

 

 




