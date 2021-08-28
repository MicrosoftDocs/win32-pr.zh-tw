---
title: 使用 AccChecker 進行測試
description: 描述合併 AccChecker 的一般測試工作流程。
ms.assetid: 18C2DDEE-D199-4C22-9ADF-1E07B1325A06
keywords:
- 使用 AccChecker 進行測試
- AccChecker，測試工作流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addf725431a17a9b63376dfc3fc7ef8563a1737c9867b950f09eb123bf7daf18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795508"
---
# <a name="testing-with-accchecker"></a>使用 AccChecker 進行測試

下列案例描述當您使用 AccChecker 進行測試時，通常會遵循的步驟。

> [!Note]  
> 當 AccChecker 驗證常式正在執行時，與主機電腦的使用者互動可能會干擾某些常式。 我們建議您在 AccChecker 通知使用者所有工作都已完成之前，不會進行進一步的使用者互動。

 

1.  在特定目標應用程式或控制項上執行 AccChecker 驗證。 如需詳細資訊，請參閱 [ [驗證]](the-accchecker-graphical-user-interface.md)索引標籤。
    > [!Note]  
    > AccChecker 不會探索應用程式中的所有 UI 排列。 在視窗、窗格、索引標籤和功能表等控制項中隱藏的元素必須以手動方式公開。

     

2.  檢查 AccChecker 錯誤記錄檔，並評估或分級結果。 修正簡單的問題，並適當地記錄嚴重的錯誤。
3.  針對可忽略的錯誤和錯誤產生隱藏專案檔，直到迴歸測試為止。
4.  使用隱藏專案檔和初始錯誤修正來重新執行 AccChecker 驗證。 這會提供目前的 Microsoft Active Accessibility 執行問題的快照集，並建立迴歸測試的基準。
5.  將 AccChecker Api 和隱藏專案整合到自動化測試架構中，以針對從初始 AccChecker 驗證記錄的 bug 進行迴歸測試。
    > [!Note]  
    > 修正錯誤時，應該視需要修改隱藏專案檔。

     

6.  確認應用程式或控制項中未引進任何回歸或新的協助工具 bug。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[UI 協助工具檢查程式](ui-accessibility-checker.md)
</dt> </dl>

 

 




