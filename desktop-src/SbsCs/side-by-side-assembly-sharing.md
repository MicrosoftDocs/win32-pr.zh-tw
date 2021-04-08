---
description: 下圖說明兩個應用程式如何使用傳統的元件共用方法共用元件。
ms.assetid: 2b9c6511-ae79-498f-a20c-ccb32a623d42
title: 並存元件共用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a94295baf2c29733c0ec366f9476a4dbf5cc3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945047"
---
# <a name="side-by-side-assembly-sharing"></a><span data-ttu-id="2f1d5-103">並存元件共用</span><span class="sxs-lookup"><span data-stu-id="2f1d5-103">Side-by-side Assembly Sharing</span></span>

<span data-ttu-id="2f1d5-104">下圖說明兩個應用程式如何使用傳統的元件共用方法共用元件。</span><span class="sxs-lookup"><span data-stu-id="2f1d5-104">The following figure illustrates how two applications might share an assembly using the traditional method of assembly sharing.</span></span> <span data-ttu-id="2f1d5-105">當應用程式安裝的元件版本（通常是 DLL）無法回溯相容時，就會發生傳統的元件共用問題。</span><span class="sxs-lookup"><span data-stu-id="2f1d5-105">A problem with traditional assembly sharing occurs when an application installs a version of an assembly—commonly a DLL—that is not backward compatible.</span></span> <span data-ttu-id="2f1d5-106">剛剛安裝的應用程式可運作，但相依于先前 DLL 版本的應用程式可能無法再運作。</span><span class="sxs-lookup"><span data-stu-id="2f1d5-106">The application just installed works, but applications that depended on the previous DLL version may no longer work.</span></span>

![代表共用元件的兩個應用程式](images/sxs1.png)

<span data-ttu-id="2f1d5-108">隔離應用程式和並存元件方案可讓相同 Win32 元件的不同版本在相同的系統上同時執行，而不會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="2f1d5-108">The isolated application and side-by-side assembly solution enables different versions of the same Win32 assembly to run at the same time on the same system without conflict.</span></span> <span data-ttu-id="2f1d5-109">藉由指定應用程式應該使用的並存元件版本，開發人員可保證其測試的設定一律會在使用者的電腦上重複。</span><span class="sxs-lookup"><span data-stu-id="2f1d5-109">By specifying which side-by-side assembly version the application should use, developers can guarantee that the configuration they test will always be duplicated on the user's computer.</span></span> <span data-ttu-id="2f1d5-110">下圖說明並列共用的位置。</span><span class="sxs-lookup"><span data-stu-id="2f1d5-110">Side-by-side sharing is illustrated in the following figure.</span></span>

![並行元件共用的執行](images/sxs2.png)

<span data-ttu-id="2f1d5-112">如需詳細資訊，請參閱 [關於隔離應用程式和並存元件](about-isolated-applications-and-side-by-side-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="2f1d5-112">For more information, see [About Isolated Applications and Side-by-side Assemblies](about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

 

 



