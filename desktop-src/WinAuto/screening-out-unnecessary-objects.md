---
title: 篩選掉不必要的物件
description: 如果您使用 [檢查] 檢查 Microsoft WordPad 配件中的簡單控制項，例如 [確定] 按鈕，您可以看到這些父視窗物件也包含數個不可見的子物件。
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb341881ee2ea503b1f74643723a1f90c8e5d1d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106996550"
---
# <a name="screening-out-unnecessary-objects"></a>篩選掉不必要的物件

如果您使用 [ [檢查](inspect-objects.md) ] 檢查 Microsoft WordPad 配件中的簡單控制項，例如 [確定] 按鈕，您可以看到這些父視窗物件也包含數個不可見的子物件。 這些隱藏的物件具有與控制項相同的視窗類別名稱，且具有 [**狀態 \_ 系統 \_ 不可見**](object-state-constants.md)的 [狀態屬性](state-property.md)。 下表列出 Microsoft Active Accessibility 為控制項建立的不可見子物件。



| Name          | 角色                                                                  | ChildCount |
|---------------|-----------------------------------------------------------------------|------------|
| 系統      | [**角色 \_ 系統 \_ 功能表列**](object-roles.md)     | 0          |
| 無          | [**角色 \_ 系統 \_ 標題列**](object-roles.md)   | 5          |
| 程式 | [**角色 \_ 系統 \_ 功能表列**](object-roles.md)     | 0          |
| 縱    | [**角色 \_ 系統 \_ 捲軸**](object-roles.md) | 5          |
| 方向  | [**角色 \_ 系統 \_ 捲軸**](object-roles.md) | 5          |
| "Size Box"    | [**角色 \_ 系統 \_ 抓住**](object-roles.md)           | 0          |



 

用戶端開發人員必須識別並篩選出這些父視窗物件和不可見的子物件，因為它們不會提供有意義的資訊給終端使用者。

 

 




