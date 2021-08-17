---
description: 任何執行緒都可以建立視窗。
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: 線上程中建立 Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2084536ff43ea4c52efb179177fe6f6c803c49b9f580b2d298b73e9b528f1a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143091"
---
# <a name="creating-windows-in-threads"></a>線上程中建立 Windows

任何執行緒都可以建立視窗。 建立視窗的執行緒擁有視窗和其相關聯的訊息佇列。 因此，執行緒必須提供訊息迴圈，以處理其訊息佇列中的訊息。 此外，您必須在該執行緒中使用 [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) 或 [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) ，而不是在其他 [等候](/windows/desktop/Sync/wait-functions)函式中使用，讓它可以處理訊息。 否則，當執行緒在等候時傳送訊息時，系統可能會變成鎖死。

[**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput)函數可以用來允許一組執行緒共用相同的輸入狀態。 藉由共用輸入狀態，執行緒就會共用使用中視窗的概念。 如此一來，一個執行緒就可以永遠啟動另一個執行緒的視窗。 這項功能也適用于在共用輸入狀態的不同執行緒所建立的視窗之間，共用焦點狀態、滑鼠捕捉狀態、鍵盤狀態和視窗迭置順序狀態。

如需建立視窗的詳細資訊，請參閱[Windows 類別](../winmsg/window-classes.md)。

 

 
