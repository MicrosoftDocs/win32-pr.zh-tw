---
title: SRSetRestorePoint 的嵌套呼叫
description: 本主題說明透過 BEGIN \_ nested \_ 系統 \_ 變更和結束 \_ 嵌套 \_ 系統 \_ 變更事件種類對 SRSetRestorePoint 進行的嵌套呼叫支援。
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5654dc7bb6e42ae55cbad18fc2418df3bdd942d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183608"
---
# <a name="nested-calls-to-srsetrestorepoint"></a>SRSetRestorePoint 的嵌套呼叫

本主題說明透過 BEGIN [](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) \_ nested \_ 系統 \_ 變更和結束 \_ 嵌套 \_ 系統 \_ 變更事件種類對 SRSetRestorePoint 進行的嵌套呼叫支援。

使用這些事件種類時，應用程式可以安全地呼叫 [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) 。 函數的第一個呼叫會建立還原點。 對函式的後續嵌套呼叫不會建立還原點。 例如，假設應用程式會對 **SRSetRestorePoint** 進行下列呼叫：<dl> 針對具有 dwEventType = BEGIN \_ NESTED \_ SYSTEM \_ 變更的還原點 A  
針對具有 dwEventType = BEGIN \_ NESTED \_ SYSTEM \_ 變更的還原點 B  
針對具有 dwEventType = END \_ NESTED \_ SYSTEM \_ 變更的還原點 B  
With dwEventType = END \_ NESTED \_ SYSTEM \_ CHANGE 的還原點 A  
</dl>

第二個呼叫不會建立新的還原點，因為呼叫是嵌套的。

 

 




