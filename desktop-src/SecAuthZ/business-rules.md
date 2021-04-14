---
description: 商務規則可讓應用程式在執行時間使用邏輯，以限定授與用戶端的許可權。
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: 商務規則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f77d94ce623086b8850406f9bae4f412d3bbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195574"
---
# <a name="business-rules"></a><span data-ttu-id="55104-103">商務規則</span><span class="sxs-lookup"><span data-stu-id="55104-103">Business Rules</span></span>

<span data-ttu-id="55104-104">商務規則可讓應用程式在執行時間使用邏輯，以限定授與用戶端的許可權。</span><span class="sxs-lookup"><span data-stu-id="55104-104">A business rule allows an application to use logic at run time to qualify permissions granted to the client.</span></span>

<span data-ttu-id="55104-105">商務規則是以 Visual Basic Scripting Edition (VBScript) 程式設計語言撰寫的腳本，或使用與 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) 物件相關聯的 Microsoft JScript 開發軟體撰寫的腳本。</span><span class="sxs-lookup"><span data-stu-id="55104-105">A business rule is a script written in the Visual Basic Scripting Edition (VBScript) programming language or written using the Microsoft JScript development software that is associated with an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object.</span></span> <span data-ttu-id="55104-106">當應用程式檢查作業的存取權時，授權管理員會先檢查目前的用戶端是否有權存取包含該作業但未與商務規則相關聯的任何工作。</span><span class="sxs-lookup"><span data-stu-id="55104-106">When an application checks access for an operation, Authorization Manager first checks if the current client has access to any tasks that contain that operation but that are not associated with business rules.</span></span> <span data-ttu-id="55104-107">如果未以此方式授與存取權，則授權管理員會執行與包含作業之任何工作相關聯的商務規則腳本。</span><span class="sxs-lookup"><span data-stu-id="55104-107">If access is not granted this way, Authorization Manager runs business-rule scripts associated with any task that contains the operation.</span></span>

<span data-ttu-id="55104-108">應用程式會將資訊傳遞至商務規則腳本，作為一組代表參數名稱和值的陣列。</span><span class="sxs-lookup"><span data-stu-id="55104-108">An application passes information to a business-rule script as a pair of arrays that represent the names and values of parameters.</span></span> <span data-ttu-id="55104-109">腳本會透過在腳本執行時所建立的 [**azbizrulecoNtext.businessruleresult**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) 物件來存取這些參數。</span><span class="sxs-lookup"><span data-stu-id="55104-109">The script has access to these parameters through an [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) object that is created when the script runs.</span></span>

<span data-ttu-id="55104-110">商務規則腳本無法指派給委派範圍所包含的工作。</span><span class="sxs-lookup"><span data-stu-id="55104-110">A business-rule script cannot be assigned to a task contained by a delegated scope.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55104-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="55104-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55104-112">在 c + + 中使用商務邏輯來限定存取權</span><span class="sxs-lookup"><span data-stu-id="55104-112">Qualifying Access with Business Logic in C++</span></span>](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



