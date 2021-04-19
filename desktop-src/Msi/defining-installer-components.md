---
description: 以下概述如何將您的應用程式組織成 Windows Installer 元件。
ms.assetid: 981a3def-1e59-4703-ad97-c8cd5431375d
title: 定義安裝程式元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ade4476fa1bf54a0ab4f64d0d43d72265ac1eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975767"
---
# <a name="defining-installer-components"></a><span data-ttu-id="cc76c-103">定義安裝程式元件</span><span class="sxs-lookup"><span data-stu-id="cc76c-103">Defining Installer Components</span></span>

<span data-ttu-id="cc76c-104">以下概述如何將您的應用程式組織成 Windows Installer 元件。</span><span class="sxs-lookup"><span data-stu-id="cc76c-104">The following outlines how to organize your application into Windows Installer components.</span></span>

<span data-ttu-id="cc76c-105">**若要將應用程式組織成元件**</span><span class="sxs-lookup"><span data-stu-id="cc76c-105">**To organize an application into components**</span></span>

1.  <span data-ttu-id="cc76c-106">從取得應用程式中使用的所有檔案和其他資源的目錄和檔案樹狀結構開始。</span><span class="sxs-lookup"><span data-stu-id="cc76c-106">Begin by obtaining a directory and file tree for all of the files and other resources used in your application.</span></span>
2.  <span data-ttu-id="cc76c-107">識別在應用程式間共用的任何檔案、登錄機碼、快捷方式或其他資源，而且可以由可作為 [合併模組](merge-modules.md)的現有元件提供。</span><span class="sxs-lookup"><span data-stu-id="cc76c-107">Identify any files, registry keys, shortcuts, or other resources that are shared across applications and can be provided by existing components available as [merge modules](merge-modules.md).</span></span> <span data-ttu-id="cc76c-108">您不能在您所撰寫的元件中包含這些資源。</span><span class="sxs-lookup"><span data-stu-id="cc76c-108">You must not include any of these resources in the components you author.</span></span> <span data-ttu-id="cc76c-109">您可以藉由合併合併模組至您的安裝套件，來取得這些元件。</span><span class="sxs-lookup"><span data-stu-id="cc76c-109">Instead obtain these components by merging the merge modules into your installation package.</span></span> <span data-ttu-id="cc76c-110">下列步驟說明如何將應用程式的其餘資源組織成元件。</span><span class="sxs-lookup"><span data-stu-id="cc76c-110">The following steps describe how to organize the remaining resources of the application into components.</span></span>
3.  <span data-ttu-id="cc76c-111">為每個 .exe、.dll 和 .ocx 檔案定義一個新元件。</span><span class="sxs-lookup"><span data-stu-id="cc76c-111">Define a new component for every .exe, .dll, and .ocx file.</span></span> <span data-ttu-id="cc76c-112">將這些檔案指定為其元件的金鑰路徑檔案。</span><span class="sxs-lookup"><span data-stu-id="cc76c-112">Designate these files as the key path files of their components.</span></span> <span data-ttu-id="cc76c-113">為每個元件指派元件程式碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="cc76c-113">Assign each component a component code GUID.</span></span>
4.  <span data-ttu-id="cc76c-114">為每個 .hlp 或 .chm 說明檔定義一個新元件。</span><span class="sxs-lookup"><span data-stu-id="cc76c-114">Define a new component for every .hlp or .chm help file.</span></span> <span data-ttu-id="cc76c-115">將這些檔案指定為其元件的金鑰路徑檔案。</span><span class="sxs-lookup"><span data-stu-id="cc76c-115">Designate these files as the key path files of their components.</span></span> <span data-ttu-id="cc76c-116">將 cnt 或..............。</span><span class="sxs-lookup"><span data-stu-id="cc76c-116">Add the .cnt or .chi files to the components holding their associated .hlp and .chm files.</span></span> <span data-ttu-id="cc76c-117">為每個元件指派元件程式碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="cc76c-117">Assign each component a component code GUID.</span></span>
5.  <span data-ttu-id="cc76c-118">針對做為快捷方式目標的每個檔案定義新元件。</span><span class="sxs-lookup"><span data-stu-id="cc76c-118">Define a new component for every file that serves as a target of a shortcut.</span></span> <span data-ttu-id="cc76c-119">將這些檔案指定為其元件的金鑰路徑檔案。</span><span class="sxs-lookup"><span data-stu-id="cc76c-119">Designate these files as the key path files of their components.</span></span> <span data-ttu-id="cc76c-120">為每個元件指派元件程式碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="cc76c-120">Assign each component a component code GUID.</span></span>
6.  <span data-ttu-id="cc76c-121">將所有剩餘的資源群組到資料夾中。</span><span class="sxs-lookup"><span data-stu-id="cc76c-121">Group all of the remaining resources into folders.</span></span> <span data-ttu-id="cc76c-122">每個資料夾中的所有資源都必須一起出貨。</span><span class="sxs-lookup"><span data-stu-id="cc76c-122">All resources in each folder must ship together.</span></span> <span data-ttu-id="cc76c-123">如果未來可能會有一組資源分開運送，請將這些資源放在不同的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="cc76c-123">If there is a possibility that a pair of resources may ship separately in the future, put these in separate folders.</span></span> <span data-ttu-id="cc76c-124">為每個資料夾定義一個新元件。</span><span class="sxs-lookup"><span data-stu-id="cc76c-124">Define a new component for every folder.</span></span> <span data-ttu-id="cc76c-125">請嘗試將元件總數保持在低，以改善效能。</span><span class="sxs-lookup"><span data-stu-id="cc76c-125">Try to keep the total number of components low to improve performance.</span></span> <span data-ttu-id="cc76c-126">需要讓安裝程式徹底檢查安裝的有效性時，將應用程式分成許多元件。</span><span class="sxs-lookup"><span data-stu-id="cc76c-126">Divide the application into many components when it is necessary to have the installer check the validity of the installation thoroughly.</span></span> <span data-ttu-id="cc76c-127">將元件中的任何檔案指定為金鑰路徑檔案。</span><span class="sxs-lookup"><span data-stu-id="cc76c-127">Designate any file in the component as the key path file.</span></span> <span data-ttu-id="cc76c-128">為每個元件指派元件程式碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="cc76c-128">Assign each component a component code GUID.</span></span>
7.  <span data-ttu-id="cc76c-129">將登錄機碼新增至元件。</span><span class="sxs-lookup"><span data-stu-id="cc76c-129">Add registry keys to the components.</span></span> <span data-ttu-id="cc76c-130">指向檔案的任何登錄機碼都應該包含在該檔案的元件中。</span><span class="sxs-lookup"><span data-stu-id="cc76c-130">Any registry key that points to a file should be included in that file's component.</span></span> <span data-ttu-id="cc76c-131">其他的登錄機碼應以邏輯方式分組需要的檔案。</span><span class="sxs-lookup"><span data-stu-id="cc76c-131">Other registry keys should be logically grouped with the files that require them.</span></span>

 

 



