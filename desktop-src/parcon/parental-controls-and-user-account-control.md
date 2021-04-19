---
description: 家長監護和使用者帳戶控制
ms.assetid: dc7c322a-f534-4dda-8c62-aa628a7b91bc
title: 家長監護和使用者帳戶控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7798661a7cadc4d497791925c83cdfa684b252a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977898"
---
# <a name="parental-controls-and-user-account-control"></a>家長監護和使用者帳戶控制

 (UAC) 的使用者帳戶控制會導致受保護的系統管理員和標準使用者帳戶存在。 受保護的系統管理員將會以標準使用者的相同許可權，在正常使用方式下執行。 針對特殊許可權作業：

-   系統會在 [認證消費者介面] 對話方塊中顯示標準使用者，這需要針對受保護的系統管理員或內建的系統管理員輸入使用者名稱和密碼。
-   [同意消費者介面] 對話方塊會顯示受保護的系統管理員，要求您選取 [允許] 繼續進行。

請務必注意，UAC 是以每個進程為基礎來執行，因此處理程式會提高許可權執行。 一般來說，它並不適合用來在永遠提高許可權的情況下執行大型應用程式的安全性觀點。 若為家長監護，必須修改設定的程式碼應由兩個執行選項的其中一個隔離：

1.  針對設定管理建立小型可執行檔，並在其資訊清單中標示為需要系統管理許可權。 叫用可執行檔會在允許進程執行之前，先顯示同意或認證 UI。
2.  提供產品 DLL 中的 COM 介面，以允許每個 UAC 檔的調用。 這也會導致適當的同意或認證 UI 顯示。

 

 



