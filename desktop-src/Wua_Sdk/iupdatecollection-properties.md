---
description: IUpdateCollection 介面會定義下列屬性。
ms.assetid: 38420d5e-4d36-4ed7-be06-e1df903929a7
title: IUpdateCollection 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aae347885deccb52ac44513bd1138aa18995c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972877"
---
# <a name="iupdatecollection-properties"></a><span data-ttu-id="0b613-103">IUpdateCollection 屬性</span><span class="sxs-lookup"><span data-stu-id="0b613-103">IUpdateCollection Properties</span></span>

<span data-ttu-id="0b613-104">[**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="0b613-104">The [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) interface defines the following properties.</span></span>



| <span data-ttu-id="0b613-105">屬性</span><span class="sxs-lookup"><span data-stu-id="0b613-105">Property</span></span>                                        | <span data-ttu-id="0b613-106">描述</span><span class="sxs-lookup"><span data-stu-id="0b613-106">Description</span></span>                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b613-107">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="0b613-107">**\_NewEnum**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get__newenum) | <span data-ttu-id="0b613-108">取得可用來列舉集合的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="0b613-108">Gets an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface that can be used to enumerate the collection.</span></span> |
| [<span data-ttu-id="0b613-109">**計數**</span><span class="sxs-lookup"><span data-stu-id="0b613-109">**Count**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_count)        | <span data-ttu-id="0b613-110">取得集合中的項目數。</span><span class="sxs-lookup"><span data-stu-id="0b613-110">Gets the number of elements in the collection.</span></span>                                                                           |
| [<span data-ttu-id="0b613-111">**項目**</span><span class="sxs-lookup"><span data-stu-id="0b613-111">**Item**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_item)          | <span data-ttu-id="0b613-112">取得或設定集合中的 [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) 介面。</span><span class="sxs-lookup"><span data-stu-id="0b613-112">Gets or sets an [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) interface in a collection.</span></span>                                                    |
| [<span data-ttu-id="0b613-113">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="0b613-113">**ReadOnly**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_readonly)  | <span data-ttu-id="0b613-114">取得布林值，這個值表示更新集合是否為唯讀。</span><span class="sxs-lookup"><span data-stu-id="0b613-114">Gets a Boolean value that indicates whether the update collection is read-only.</span></span>                                          |



 

 

 
