---
title: '[系統還原]'
description: 設定系統還原點，並監視程式的主要系統變更，讓系統回復為先前的狀態。 撰寫自動復原程式碼或 wmi 腳本，將系統狀態還原到已註冊的還原點。
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- '[系統還原]'
- 系統還原，起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bdc4555171ad867f6e6b925144d9ed673ffc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092892"
---
# <a name="system-restore"></a>[系統還原]

## <a name="purpose"></a>目的

系統還原會自動監視並記錄使用者電腦上的重要系統變更。 其設計目的是為了降低支援成本，並讓使用者復原可能造成系統問題的變更，或在系統以最佳方式執行時還原為一天，以提高客戶滿意度。

> [!Note]  
> 下列檔是針對開發人員所設計的。 如果您是使用者尋找如何使用系統還原的相關資訊，請參閱 [系統還原是什麼？](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)

 

## <a name="developer-audience"></a>開發人員對象

系統還原 API 是設計來供 C/c + + 程式設計人員使用。 使用指令碼介面需要熟悉 Windows Management Instrumentation (WMI) 。

## <a name="run-time-requirements"></a>執行階段需求求

自 Windows XP 起的用戶端作業系統支援系統還原 API。 如需有關使用特定 API 專案所需之作業系統的詳細資訊，請參閱其檔的需求一節。

## <a name="in-this-section"></a>本節內容



| 主題                                                | 描述                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [概觀](about-system-restore.md)<br/>      | 概述系統還原的運作方式。<br/>                            |
| [參考](system-restore-reference.md)<br/> | 系統還原函數、結構和類別的檔。<br/> |
| [範例](using-system-restore.md)<br/>       | 以 C 撰寫的範例程式。<br/>                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

