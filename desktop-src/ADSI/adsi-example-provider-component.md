---
title: ADSI 範例提供者元件
description: Active Directory 服務介面提供者寫入器將會發現這是特別感興趣的部分，因為它說明了 ADSI 範例提供者元件的深度。
ms.assetid: 1ca73817-7a21-4a39-b496-fc82db26ea4e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7bf960021df9a3b26f252584cad2ff3374254a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300104"
---
# <a name="adsi-example-provider-component"></a><span data-ttu-id="3215c-103">ADSI 範例提供者元件</span><span class="sxs-lookup"><span data-stu-id="3215c-103">ADSI Example Provider Component</span></span>

<span data-ttu-id="3215c-104">Active Directory 服務介面提供者寫入器將會發現這是特別感興趣的部分，因為它說明了 ADSI 範例提供者元件的深度。</span><span class="sxs-lookup"><span data-stu-id="3215c-104">Active Directory Service Interfaces provider writers will find this section of particular interest, because it describes the ADSI example provider component in depth.</span></span> <span data-ttu-id="3215c-105">ADSI 提供者寫入器可以安裝範例提供者，並使用程式碼架構作為基礎來建立自己的實作為基礎。</span><span class="sxs-lookup"><span data-stu-id="3215c-105">ADSI provider writers can install the example provider and use the code framework as a basis to create their own implementation.</span></span> <span data-ttu-id="3215c-106">我們將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="3215c-106">The following topics are discussed:</span></span>

<span data-ttu-id="3215c-107">[安裝範例提供者元件](installing-the-example-provider-component.md) 會說明如何安裝 ADSI 範例提供者和其 mock 目錄。</span><span class="sxs-lookup"><span data-stu-id="3215c-107">[Installing the Example Provider Component](installing-the-example-provider-component.md) describes how to install the ADSI sample provider and its mock directory.</span></span> <span data-ttu-id="3215c-108">本節包含登錄設定的清單。</span><span class="sxs-lookup"><span data-stu-id="3215c-108">This section includes a list of the registry settings.</span></span>

<span data-ttu-id="3215c-109">[目錄定義](directory-definition.md) 描述範例提供者元件所定義的目錄專案。</span><span class="sxs-lookup"><span data-stu-id="3215c-109">[Directory Definition](directory-definition.md) describes the directory entries defined by the example provider component.</span></span>

<span data-ttu-id="3215c-110">[架構管理](schema-management.md) 描述如何以特定類型的 Active Directory 物件來表示範例提供者元件目錄服務中的每個元素。</span><span class="sxs-lookup"><span data-stu-id="3215c-110">[Schema Management](schema-management.md) describes how each element in the example provider component directory service can be represented by a specific type of Active Directory object.</span></span>

<span data-ttu-id="3215c-111">系結[至 Active Directory 物件](binding-to-an-active-directory-object.md)會描述如何在給定 ADsPath 字串、範例提供者元件識別該專案、為其建立適當的 Active Directory 物件類型，以及在該物件上抓取要求的介面指標類型，以傳回到 ADs 用戶端軟體。</span><span class="sxs-lookup"><span data-stu-id="3215c-111">[Binding to an Active Directory Object](binding-to-an-active-directory-object.md) describes how, given an ADsPath string, the example provider component identifies that element, creates the appropriate type of Active Directory object for it, and retrieves the requested type of interface pointer on that object to pass back to the ADs client software.</span></span>

<span data-ttu-id="3215c-112">列舉值[物件](enumerator-objects.md)會列出由範例提供者元件提供的特定列舉型別，以及可以在其中找到執行程式碼的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="3215c-112">[Enumerator Objects](enumerator-objects.md) lists the specific types of enumerations supplied by the example provider component and in which source code the implementations can be found.</span></span>

<span data-ttu-id="3215c-113">程式[代碼總覽](code-overview.md)提供範例提供者元件中每個部分的工作層級描述。</span><span class="sxs-lookup"><span data-stu-id="3215c-113">[Code Overview](code-overview.md) provides a task-level description of each part of the example provider component.</span></span>

<span data-ttu-id="3215c-114">程式[代碼詳細資料](code-details.md)會列出軟體模組及其內容。</span><span class="sxs-lookup"><span data-stu-id="3215c-114">[Code Details](code-details.md) lists the software modules and their contents.</span></span>

 

 




