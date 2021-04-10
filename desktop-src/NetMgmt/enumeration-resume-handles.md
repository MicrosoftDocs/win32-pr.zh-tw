---
title: 列舉 Resume 控制碼
description: 列舉 resume 控制碼是函數實例資料中包含之實際 resume 索引鍵的識別碼。 這是安全性和互通性的必要項，可簡化函式的呼叫端程式碼。
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f20e7a7d5e1f9afb15e6adad4c0d7643bf841d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932243"
---
# <a name="enumeration-resume-handles"></a><span data-ttu-id="926f7-104">列舉 Resume 控制碼</span><span class="sxs-lookup"><span data-stu-id="926f7-104">Enumeration Resume Handles</span></span>

<span data-ttu-id="926f7-105">列舉 resume 控制碼是函數實例資料中包含之實際 resume 索引鍵的識別碼。</span><span class="sxs-lookup"><span data-stu-id="926f7-105">Enumeration resume handles are identifiers for the actual resume key contained in the instance data for the function.</span></span> <span data-ttu-id="926f7-106">這是安全性和互通性的必要項，可簡化函式的呼叫端程式碼。</span><span class="sxs-lookup"><span data-stu-id="926f7-106">This is required for security, interoperability, and to simplify the caller code for the function.</span></span>

<span data-ttu-id="926f7-107">如果傳遞給 resume 控制碼的指標的 **Null 是 Null** ，則不會儲存任何控制碼，且列舉搜尋無法繼續。</span><span class="sxs-lookup"><span data-stu-id="926f7-107">If a **NULL** is passed for the pointer to the resume handle, no handle is stored and the enumeration search cannot be continued.</span></span> <span data-ttu-id="926f7-108">這在應用程式不想列舉所有專案的情況下很有用。</span><span class="sxs-lookup"><span data-stu-id="926f7-108">This is useful in cases where the application does not want to enumerate all the items.</span></span>

<span data-ttu-id="926f7-109">如果從列舉呼叫傳回錯誤，則必須將 resume 控制碼視為無效，且不會用於任何後續的列舉呼叫。</span><span class="sxs-lookup"><span data-stu-id="926f7-109">If an error is returned from an enumeration call, the resume handle must be treated as invalid and not used for any subsequent enumeration calls.</span></span> <span data-ttu-id="926f7-110">發生這種情況時，您必須從頭重新開機列舉。</span><span class="sxs-lookup"><span data-stu-id="926f7-110">When this occurs you must restart the enumeration from the beginning.</span></span>

 

 




