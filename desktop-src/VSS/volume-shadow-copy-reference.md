---
description: 磁碟區陰影複製服務 (VSS) 是一組 COM 和 c + + Api，可讓您在系統上的應用程式 (呼叫寫入器時執行磁片區備份，) 繼續寫入磁片區。
ms.assetid: 94d9504b-2838-4516-8031-daa7bd9d2fec
title: 磁片區陰影複製 API 參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8651c987c01ce67f1383f2ab1a24ca3fea8bbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511524"
---
# <a name="volume-shadow-copy-api-reference"></a><span data-ttu-id="01362-103">磁片區陰影複製 API 參考</span><span class="sxs-lookup"><span data-stu-id="01362-103">Volume Shadow Copy API Reference</span></span>

<span data-ttu-id="01362-104">磁碟區陰影複製服務 (VSS) 是一組 COM 和 c + + Api，可讓您在系統上的應用程式 (呼叫寫入器時執行磁片區備份，) 繼續寫入磁片區。</span><span class="sxs-lookup"><span data-stu-id="01362-104">The Volume Shadow Copy Service (VSS) is a set of COM and C++ APIs that enable volume backups to be performed while applications on the system (called writers) continue to write to the volumes.</span></span>

<span data-ttu-id="01362-105">VSS 透過建立陰影複製，在指定的時間點複製原始磁片區，以支援這些備份。</span><span class="sxs-lookup"><span data-stu-id="01362-105">VSS supports these backups through the creation of shadow copies, a duplicate of the original volume at a given point in time.</span></span>

<span data-ttu-id="01362-106">協力廠商開發人員可以使用 VSS API 來建立要求者 (例如備份應用程式) 建立及管理陰影複製。</span><span class="sxs-lookup"><span data-stu-id="01362-106">Third-party developers can use the VSS API to create requesters (such as a backup application) to create and manage shadow copies.</span></span>

<span data-ttu-id="01362-107">建立和表示陰影複製的實際工作，是由稱為提供者的系統層級應用程式進行。</span><span class="sxs-lookup"><span data-stu-id="01362-107">The actual work of creating and representing shadow copies is conducted by system-level applications known as providers.</span></span>

<span data-ttu-id="01362-108">開發人員也可以使用 API 來設計寫入器：可透過 VSS 感知的應用程式，使用陰影複製的建立和操作來協調 i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="01362-108">Developers can also use the API to construct writers: VSS-aware applications that are able to coordinate I/O operations with the creation and manipulation of shadow copies.</span></span>

-   [<span data-ttu-id="01362-109">磁片區陰影複製 API 類別</span><span class="sxs-lookup"><span data-stu-id="01362-109">Volume Shadow Copy API Classes</span></span>](volume-shadow-copy-api-classes.md)
-   [<span data-ttu-id="01362-110">磁片區陰影複製 API 資料類型</span><span class="sxs-lookup"><span data-stu-id="01362-110">Volume Shadow Copy API Data Types</span></span>](volume-shadow-copy-api-data-types.md)
-   [<span data-ttu-id="01362-111">磁片區陰影複製 API 列舉</span><span class="sxs-lookup"><span data-stu-id="01362-111">Volume Shadow Copy API Enumerations</span></span>](volume-shadow-copy-api-enumeration-types.md)
-   [<span data-ttu-id="01362-112">磁片區陰影複製 API 函數</span><span class="sxs-lookup"><span data-stu-id="01362-112">Volume Shadow Copy API Functions</span></span>](volume-shadow-copy-api-functions.md)
-   [<span data-ttu-id="01362-113">磁片區陰影複製 API 介面</span><span class="sxs-lookup"><span data-stu-id="01362-113">Volume Shadow Copy API Interfaces</span></span>](volume-shadow-copy-api-interfaces.md)
-   [<span data-ttu-id="01362-114">磁片區陰影複製 API 結構</span><span class="sxs-lookup"><span data-stu-id="01362-114">Volume Shadow Copy API Structures</span></span>](volume-shadow-copy-api-structures.md)
-   [<span data-ttu-id="01362-115">磁片區陰影複製詞彙</span><span class="sxs-lookup"><span data-stu-id="01362-115">Volume Shadow Copy Glossary</span></span>](volume-shadow-copy-glossary.md)

<span data-ttu-id="01362-116">如需撰寫要求者和寫入器的詳細資訊，請參閱 [使用磁碟區陰影複製服務](using-the-volume-shadow-copy-service.md)。</span><span class="sxs-lookup"><span data-stu-id="01362-116">For more information on writing requesters and writers, see [Using the Volume Shadow Copy Service](using-the-volume-shadow-copy-service.md).</span></span>

 

 



