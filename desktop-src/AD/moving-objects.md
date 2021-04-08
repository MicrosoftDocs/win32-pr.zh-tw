---
title: 移動物件
description: 移動物件
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，移動物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7019904d0de42492b98ddd297ab007a6f4e52f6a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023233"
---
# <a name="moving-objects"></a><span data-ttu-id="f59d0-104">移動物件</span><span class="sxs-lookup"><span data-stu-id="f59d0-104">Moving Objects</span></span>

<span data-ttu-id="f59d0-105">若要移動網域內的物件，請使用 [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) 方法。</span><span class="sxs-lookup"><span data-stu-id="f59d0-105">To move an object within a domain, use the [**IADsContainer.MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) method.</span></span>

<span data-ttu-id="f59d0-106">**移動網域內的物件**</span><span class="sxs-lookup"><span data-stu-id="f59d0-106">**To move an object within a domain**</span></span>

1.  <span data-ttu-id="f59d0-107">系結至要移動之物件的 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 介面。</span><span class="sxs-lookup"><span data-stu-id="f59d0-107">Bind to the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface of the object to move.</span></span>
2.  <span data-ttu-id="f59d0-108">取得物件的 ADsPath 以從 [**IADs**](/windows/desktop/ADSI/iads-property-methods) 屬性移動。</span><span class="sxs-lookup"><span data-stu-id="f59d0-108">Get the ADsPath of the object to move from the [**IADs.ADsPath**](/windows/desktop/ADSI/iads-property-methods) property.</span></span>
3.  <span data-ttu-id="f59d0-109">系結至將移至物件的容器的 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 介面。</span><span class="sxs-lookup"><span data-stu-id="f59d0-109">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface of the container where the object will be moved to.</span></span>
4.  <span data-ttu-id="f59d0-110">使用 [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) 方法移動物件。</span><span class="sxs-lookup"><span data-stu-id="f59d0-110">Move the object with the [**IADsContainer.MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) method.</span></span>

<span data-ttu-id="f59d0-111">如果已移動的物件有介面，則在移動物件之後，介面會無效，因為介面表示的目錄物件已不存在。</span><span class="sxs-lookup"><span data-stu-id="f59d0-111">If an interface exists to the object that was moved, the interface is not valid after the object is moved because the directory object the interface represents no longer exists.</span></span>

<span data-ttu-id="f59d0-112">如需顯示如何移動物件的詳細資訊和程式碼範例，請參閱 [移動物件的範例程式碼](example-code-for-moving-an-object.md)。</span><span class="sxs-lookup"><span data-stu-id="f59d0-112">For more information and a code example that shows how to move an object, see [Example Code for Moving an Object](example-code-for-moving-an-object.md).</span></span>

 

 