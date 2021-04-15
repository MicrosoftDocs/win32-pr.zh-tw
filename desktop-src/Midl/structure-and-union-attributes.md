---
title: Structure 和 Union 屬性
description: 使用 switch \_ \ 屬性可指定遠端程序呼叫中聯集的特性。 您可以使用 [略過] 屬性，將某些結構或等位成員指定為用戶端應用程式的本機。
ms.assetid: e06e5184-fa92-4446-964b-d56d0e5f2872
keywords:
- IDL MIDL、屬性、結構和等位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2a7764d56c8557bd71923021a9f324a118ac81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462157"
---
# <a name="structure-and-union-attributes"></a><span data-ttu-id="1c24f-105">Structure 和 Union 屬性</span><span class="sxs-lookup"><span data-stu-id="1c24f-105">Structure and Union Attributes</span></span>

<span data-ttu-id="1c24f-106">使用 **switch \_** \* 屬性可指定遠端程序呼叫中聯集的特性。</span><span class="sxs-lookup"><span data-stu-id="1c24f-106">Use the **switch\_**\* attributes to specify the characteristic of a union in a remote procedure call.</span></span> <span data-ttu-id="1c24f-107">您可以使用 [ [**略**](ignore.md) 過] 屬性，將某些結構或等位成員指定為用戶端應用程式的本機。</span><span class="sxs-lookup"><span data-stu-id="1c24f-107">Use the [**ignore**](ignore.md) attribute to designate certain structure or union members as local to the client application.</span></span>



| <span data-ttu-id="1c24f-108">屬性</span><span class="sxs-lookup"><span data-stu-id="1c24f-108">Attribute</span></span>                           | <span data-ttu-id="1c24f-109">使用方式</span><span class="sxs-lookup"><span data-stu-id="1c24f-109">Usage</span></span>                                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c24f-110">**開關**</span><span class="sxs-lookup"><span data-stu-id="1c24f-110">**switch**</span></span>](switch.md)            | <span data-ttu-id="1c24f-111">選取封裝聯集的判別。</span><span class="sxs-lookup"><span data-stu-id="1c24f-111">Selects the discriminant for an encapsulated union.</span></span>                                                                           |
| [<span data-ttu-id="1c24f-112">**切換 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="1c24f-112">**switch\_is**</span></span>](switch-is.md)     | <span data-ttu-id="1c24f-113">識別 nonencapsulated 聯集的判別。</span><span class="sxs-lookup"><span data-stu-id="1c24f-113">Identifies the discriminant for a nonencapsulated union.</span></span>                                                                      |
| [<span data-ttu-id="1c24f-114">**切換 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="1c24f-114">**switch\_type**</span></span>](switch-type.md) | <span data-ttu-id="1c24f-115">識別 nonencapsulated 聯集的判別類型。</span><span class="sxs-lookup"><span data-stu-id="1c24f-115">Identifies the type of the discriminant for a nonencapsulated union.</span></span>                                                          |
| [<span data-ttu-id="1c24f-116">**忽略**</span><span class="sxs-lookup"><span data-stu-id="1c24f-116">**ignore**</span></span>](ignore.md)            | <span data-ttu-id="1c24f-117">指定包含在結構或等位中的指標，以及指標所指出的物件不會傳送。</span><span class="sxs-lookup"><span data-stu-id="1c24f-117">Designates that a pointer contained in a structure or union and the object indicated by the pointer is not to be transmitted.</span></span> |



 

<span data-ttu-id="1c24f-118">您也可以使用 [陣列和調整大小的指標屬性](array-and-sized-pointer-attributes.md) 來指定結構或等位成員的特性。</span><span class="sxs-lookup"><span data-stu-id="1c24f-118">You can also use the [array and sized pointer attributes](array-and-sized-pointer-attributes.md) to specify characteristics of structure or union members.</span></span>

 

 




