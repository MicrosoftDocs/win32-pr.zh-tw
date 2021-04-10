---
title: 連結到遠端存取 DLL
description: 如果應用程式以靜態方式連結至 RASAPI32 DLL，則如果未安裝遠端存取服務，應用程式將無法載入。
ms.assetid: a2399406-f73c-40aa-877c-80f2f99ed10a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd8b29eab4bf2cd7689836e9310a3c0f6370dfb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842552"
---
# <a name="linking-to-the-remote-access-dll"></a><span data-ttu-id="a2ccc-103">連結到遠端存取 DLL</span><span class="sxs-lookup"><span data-stu-id="a2ccc-103">Linking to the Remote Access DLL</span></span>

<span data-ttu-id="a2ccc-104">如果應用程式以靜態方式連結至 RASAPI32 DLL，則如果未安裝遠端存取服務，應用程式將無法載入。</span><span class="sxs-lookup"><span data-stu-id="a2ccc-104">If an application links statically to the RASAPI32 DLL, the application will fail to load if Remote Access Service is not installed.</span></span> <span data-ttu-id="a2ccc-105">如果未使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 來載入 DLL，則可以載入 ras 應用程式，並使用 [**GETPROCADDRESS**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 來取得 ras 函式的指標。</span><span class="sxs-lookup"><span data-stu-id="a2ccc-105">A RAS application can load when RAS is not installed by using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) to load the DLL, and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain pointers to the RAS functions.</span></span>

<span data-ttu-id="a2ccc-106">RAS 函數位于 RASAPI32.DLL 中。</span><span class="sxs-lookup"><span data-stu-id="a2ccc-106">The RAS functions are located in RASAPI32.DLL.</span></span> <span data-ttu-id="a2ccc-107">這些函數的匯入程式庫是 RASAPI32。自由。</span><span class="sxs-lookup"><span data-stu-id="a2ccc-107">The import library for these functions is RASAPI32.LIB.</span></span> <span data-ttu-id="a2ccc-108">若要使用 RAS 功能，您的程式必須包含下列檔案：</span><span class="sxs-lookup"><span data-stu-id="a2ccc-108">To use the RAS functions, your programs must include the following files:</span></span>



| <span data-ttu-id="a2ccc-109">檔案</span><span class="sxs-lookup"><span data-stu-id="a2ccc-109">File</span></span>       | <span data-ttu-id="a2ccc-110">描述</span><span class="sxs-lookup"><span data-stu-id="a2ccc-110">Description</span></span>                                                                 |
|------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a2ccc-111">Ras。H</span><span class="sxs-lookup"><span data-stu-id="a2ccc-111">RAS.H</span></span>      | <span data-ttu-id="a2ccc-112">包含 RAS 函數原型、常數和結構定義。</span><span class="sxs-lookup"><span data-stu-id="a2ccc-112">Contains the RAS function prototypes, constants, and structure definitions.</span></span> |
| <span data-ttu-id="a2ccc-113">RASERROR.H</span><span class="sxs-lookup"><span data-stu-id="a2ccc-113">RASERROR.H</span></span> | <span data-ttu-id="a2ccc-114">包含 RAS 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a2ccc-114">Contains the RAS error codes.</span></span>                                               |



 

 

 