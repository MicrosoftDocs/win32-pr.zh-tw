---
description: 當安裝 Windows Installer 套件時不需要提高許可權時，套件的作者可以隱藏 [使用者帳戶控制] (UAC) 顯示的對話方塊，以提示使用者提供系統管理員授權。
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: 在不含 UAC 對話方塊的情況下撰寫套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5064589a49327db263158b10ff9377e0f7b69232b0e3679d5bd86c7bd2f2e3f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066088"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a>在不含 UAC 對話方塊的情況下撰寫套件

當安裝 Windows Installer 套件時不需要提高許可權時，套件的作者可以隱藏 [[*使用者帳戶控制*](u-gly.md)] (UAC) 顯示的對話方塊，以提示使用者提供系統管理員授權。

若要在安裝應用程式時抑制 UAC 對話方塊的顯示，封裝的作者應該執行下列作業：

-   使用 windows Installer 4.0 或更新版本，在 Windows Vista 中安裝應用程式。
-   請勿依賴使用提升的系統許可權在電腦上安裝應用程式。
-   在每個使用者的內容中安裝應用程式，並使其成為封裝的預設安裝內容。 如果未設定 [**ALLUSERS**](allusers.md) 屬性，安裝程式就會在每個使用者的內容中安裝套件。 如果您未在 [屬性工作表](property-table.md)中包含 **ALLUSERS** 屬性，安裝程式就不會設定這個屬性，因此每個使用者安裝都會變成預設的安裝內容。 您可以藉由在命令列上設定 **ALLUSERS** 屬性來覆寫這個預設值。
-   在 [ [**字數統計摘要**](word-count-summary.md) ] 屬性中設定位3，表示安裝應用程式時不需要提高的許可權。

 

 



