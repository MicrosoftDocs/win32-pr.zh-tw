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
# <a name="parental-controls-and-user-account-control"></a><span data-ttu-id="b0db4-103">家長監護和使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="b0db4-103">Parental Controls and User Account Control</span></span>

<span data-ttu-id="b0db4-104"> (UAC) 的使用者帳戶控制會導致受保護的系統管理員和標準使用者帳戶存在。</span><span class="sxs-lookup"><span data-stu-id="b0db4-104">User Account Control (UAC) will result in presence of Protected Administrator and Standard User accounts.</span></span> <span data-ttu-id="b0db4-105">受保護的系統管理員將會以標準使用者的相同許可權，在正常使用方式下執行。</span><span class="sxs-lookup"><span data-stu-id="b0db4-105">A Protected Administrator will run with the same rights as a Standard User under normal usage.</span></span> <span data-ttu-id="b0db4-106">針對特殊許可權作業：</span><span class="sxs-lookup"><span data-stu-id="b0db4-106">For privileged operations:</span></span>

-   <span data-ttu-id="b0db4-107">系統會在 [認證消費者介面] 對話方塊中顯示標準使用者，這需要針對受保護的系統管理員或內建的系統管理員輸入使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="b0db4-107">A Standard User will be shown the Credentials User Interface dialog box, which requires the input of a user name and password for a Protected Administrator or built-in Administrator.</span></span>
-   <span data-ttu-id="b0db4-108">[同意消費者介面] 對話方塊會顯示受保護的系統管理員，要求您選取 [允許] 繼續進行。</span><span class="sxs-lookup"><span data-stu-id="b0db4-108">A Protected Administrator will be shown the Consent User Interface dialog box, which requires selection of Allow to proceed.</span></span>

<span data-ttu-id="b0db4-109">請務必注意，UAC 是以每個進程為基礎來執行，因此處理程式會提高許可權執行。</span><span class="sxs-lookup"><span data-stu-id="b0db4-109">It is important to note that UAC is implemented on a per-process basis, so a process either runs elevated or not.</span></span> <span data-ttu-id="b0db4-110">一般來說，它並不適合用來在永遠提高許可權的情況下執行大型應用程式的安全性觀點。</span><span class="sxs-lookup"><span data-stu-id="b0db4-110">Generally, it is not suitable from a security standpoint to run large applications as always elevated.</span></span> <span data-ttu-id="b0db4-111">若為家長監護，必須修改設定的程式碼應由兩個執行選項的其中一個隔離：</span><span class="sxs-lookup"><span data-stu-id="b0db4-111">For Parental Controls, code that must modify settings should be isolated by one of two implementation options:</span></span>

1.  <span data-ttu-id="b0db4-112">針對設定管理建立小型可執行檔，並在其資訊清單中標示為需要系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="b0db4-112">Create a small executable for settings management that is marked in its manifest as requiring administrative rights.</span></span> <span data-ttu-id="b0db4-113">叫用可執行檔會在允許進程執行之前，先顯示同意或認證 UI。</span><span class="sxs-lookup"><span data-stu-id="b0db4-113">Invocation of the executable will cause the Consent or Credentials UI to be shown prior to allowing the process to run.</span></span>
2.  <span data-ttu-id="b0db4-114">提供產品 DLL 中的 COM 介面，以允許每個 UAC 檔的調用。</span><span class="sxs-lookup"><span data-stu-id="b0db4-114">Provide COM interfaces in a product DLL that allow for invocation per UAC documentation.</span></span> <span data-ttu-id="b0db4-115">這也會導致適當的同意或認證 UI 顯示。</span><span class="sxs-lookup"><span data-stu-id="b0db4-115">This will also cause the appropriate Consent or Credentials UI to be shown.</span></span>

 

 



