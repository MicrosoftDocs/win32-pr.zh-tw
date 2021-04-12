---
description: 本主題說明如何建立網路監視器 SDK 隨附的一般專家。
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: 打造專家
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ead0ff222b72c66bfc88ec477d1a8d6a941273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192636"
---
# <a name="building-an-expert"></a><span data-ttu-id="dd226-103">打造專家</span><span class="sxs-lookup"><span data-stu-id="dd226-103">Building an Expert</span></span>

<span data-ttu-id="dd226-104">本主題說明如何建立網路監視器 SDK 隨附的一般專家。</span><span class="sxs-lookup"><span data-stu-id="dd226-104">This topic describes how to build a generic expert that ships with the Network Monitor SDK.</span></span>

> [!Note]  
> <span data-ttu-id="dd226-105">在建立下列程式碼範例之前，請先安裝網路監視器 SDK 並初始化 MySetEnv.bat 檔。</span><span class="sxs-lookup"><span data-stu-id="dd226-105">Before creating the following code examples, install the Network Monitor SDK and initialize the MySetEnv.bat file.</span></span>

 

<span data-ttu-id="dd226-106">**打造一般專家**</span><span class="sxs-lookup"><span data-stu-id="dd226-106">**To build a generic expert**</span></span>

1.  <span data-ttu-id="dd226-107">開啟網路監視器命令提示字元，然後流覽至 \\ 專家子目錄; 例如，C： \\ Program Files \\ NetMonSDK2 \\ 專家。</span><span class="sxs-lookup"><span data-stu-id="dd226-107">Open a Network Monitor command prompt and navigate to the \\Experts subdirectory; for example, C:\\Program Files\\NetMonSDK2\\Experts.</span></span>
2.  <span data-ttu-id="dd226-108">輸入 **xcopy/e/s/V Blrplate MyExpert**;然後，在出現提示時，輸入 **D**。</span><span class="sxs-lookup"><span data-stu-id="dd226-108">Type **xcopy /e /s /v Blrplate MyExpert**; then, when prompted, type **D**.</span></span>
3.  <span data-ttu-id="dd226-109">移至 \\ MyExpert 子目錄。</span><span class="sxs-lookup"><span data-stu-id="dd226-109">Move to the \\MyExpert subdirectory.</span></span>
4.  <span data-ttu-id="dd226-110">輸入 **Ren Blrplate \* 。 \*MyExpert \* ... \***</span><span class="sxs-lookup"><span data-stu-id="dd226-110">Type **ren Blrplate\*.\* MyExpert\*.\***.</span></span> <span data-ttu-id="dd226-111">確定已正確地重新命名所有檔案。</span><span class="sxs-lookup"><span data-stu-id="dd226-111">Ensure that all files are properly renamed.</span></span> <span data-ttu-id="dd226-112">藉由比較 \\ 專家 Blrplate 子目錄中的檔案來驗證檔案名 \\ 。</span><span class="sxs-lookup"><span data-stu-id="dd226-112">Verify the file names by comparing the files in the \\Experts\\Blrplate subdirectory.</span></span>
5.  <span data-ttu-id="dd226-113">使用 **MyExpert** 取代所有出現的 **Blrplate** ，以編輯 Makefile。</span><span class="sxs-lookup"><span data-stu-id="dd226-113">Edit the Makefile by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span>
6.  <span data-ttu-id="dd226-114">使用 **MyExpert** 取代所有出現的 **Blrplate** ，以編輯 .cpp 檔案。</span><span class="sxs-lookup"><span data-stu-id="dd226-114">Edit both .cpp files by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span> <span data-ttu-id="dd226-115">請注意，在 Config.xml 中的對話方塊識別碼必須是大寫 (例如， **MYEXPERT**) 。</span><span class="sxs-lookup"><span data-stu-id="dd226-115">Be aware that the dialog box identifier in Config.cpp must be capitalized (for example, **MYEXPERT**).</span></span>
7.  <span data-ttu-id="dd226-116">以 **MyExpert** 取代所有出現的 **Blrplate** ，以編輯 MyExpert。</span><span class="sxs-lookup"><span data-stu-id="dd226-116">Edit MyExpert.h by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span>
8.  <span data-ttu-id="dd226-117">將 **BLRPLATE** 重新命名為 **MYEXPERT**，以編輯 Resrc1。</span><span class="sxs-lookup"><span data-stu-id="dd226-117">Edit Resrc1.h by renaming **BLRPLATE** to **MYEXPERT**.</span></span> <span data-ttu-id="dd226-118"> (記住， **MYEXPERT** 必須是大寫) 。</span><span class="sxs-lookup"><span data-stu-id="dd226-118">(Remember, **MYEXPERT** must be capitalized).</span></span>
9.  <span data-ttu-id="dd226-119">將 [ **idd \_ BLRPLATE \_ config \_ ] 對話方塊** 重新命名為 [ **idd \_ MyExpert \_ config \_ ] 對話方塊**，以編輯 MyExpert .rc 檔。</span><span class="sxs-lookup"><span data-stu-id="dd226-119">Edit the MyExpert.rc file by renaming **IDD\_BLRPLATE\_CONFIG\_DIALOG** to **IDD\_MYEXPERT\_CONFIG\_DIALOG**.</span></span>
10. <span data-ttu-id="dd226-120">輸入 **nmake** 來建立 DLL 檔案。</span><span class="sxs-lookup"><span data-stu-id="dd226-120">Type **nmake** to build the DLL file.</span></span> <span data-ttu-id="dd226-121">若要驗證組建，請將目錄變更為 \\ Obj 子目錄，並確認該檔案存在。</span><span class="sxs-lookup"><span data-stu-id="dd226-121">To verify the build, change directory to the \\Obj subdirectory and verify that the file exists.</span></span> <span data-ttu-id="dd226-122">如需詳細資訊，請參閱 [觀看專家 DLL 屬性](viewing-expert-dll-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="dd226-122">For more information, see [Viewing Expert DLL Properties](viewing-expert-dll-properties.md).</span></span>

<span data-ttu-id="dd226-123">當組建完成時，您將會有一個專家 DLL，您可以使用網路監視器進行測試和部署。</span><span class="sxs-lookup"><span data-stu-id="dd226-123">When the build is complete, you will have an expert DLL that you can test and deploy with Network Monitor.</span></span> <span data-ttu-id="dd226-124">如需有關安裝專家的詳細資訊，請參閱 [安裝專家至網路監視器 2.1](installing-an-expert-to-network-monitor-2-1.md)。</span><span class="sxs-lookup"><span data-stu-id="dd226-124">For more information about installing an expert, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span> <span data-ttu-id="dd226-125">如需有關如何偵測專家的詳細資訊，請參閱 [將專家進行調試](debugging-an-expert.md)。</span><span class="sxs-lookup"><span data-stu-id="dd226-125">For more information about debugging an expert, see [Debugging an Expert](debugging-an-expert.md).</span></span>

 

 



