---
title: 存取控制和寫入作業
description: 如果呼叫端沒有足夠的許可權，屬性修改就會失敗。
ms.assetid: eb5b97fb-4654-444e-9f5a-9a4be27ef1a3
ms.tgt_platform: multiple
keywords:
- 存取控制和寫入器作業 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b8ecab475cd5696a98c985f92ccc24b1dd6072
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842011"
---
# <a name="access-control-and-write-operations"></a><span data-ttu-id="17732-104">存取控制和寫入作業</span><span class="sxs-lookup"><span data-stu-id="17732-104">Access Control and Write Operations</span></span>

<span data-ttu-id="17732-105">如果呼叫端沒有足夠的許可權，屬性修改就會失敗。</span><span class="sxs-lookup"><span data-stu-id="17732-105">Property modifications fail if the caller does not have sufficient rights.</span></span> <span data-ttu-id="17732-106">對於批次修改多個屬性的寫入作業而言，如果呼叫端沒有修改過的其中一個屬性的必要許可權，則整個作業都會失敗。</span><span class="sxs-lookup"><span data-stu-id="17732-106">For write operations that batch modifications to multiple properties, the entire operation fails if the caller does not have the necessary rights to a single one of the modified properties.</span></span> <span data-ttu-id="17732-107">例如，您可以建立多個 [**IADs：:P**](/windows/desktop/api/iads/nf-iads-iads-put) 不等的呼叫來設定物件上的多個屬性。</span><span class="sxs-lookup"><span data-stu-id="17732-107">For example, you can make multiple [**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put) calls to set multiple properties on an object.</span></span> <span data-ttu-id="17732-108">但是，當您呼叫 [**IADs：： SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 將新的資料從本機快取寫入至目錄時，如果呼叫端沒有所有修改屬性的寫入權限，則 **SetInfo** 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="17732-108">However, when you call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to write the new data from the local cache to the directory, **SetInfo** will fail if the caller does not have write access to all the modified properties.</span></span> <span data-ttu-id="17732-109">同樣地，如果呼叫端沒有所設定之所有屬性的存取權， [**IDirectoryObject：： SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) 方法就無法設定任何屬性。</span><span class="sxs-lookup"><span data-stu-id="17732-109">Similarly, the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) method fails to set any properties if the caller does not have access to all the properties being set.</span></span> <span data-ttu-id="17732-110">因此，只有在您知道所有修改都將成功時，才應該批次處理多個修改作業。</span><span class="sxs-lookup"><span data-stu-id="17732-110">So you should batch multiple modify operations only if you know that all modifications will succeed.</span></span> <span data-ttu-id="17732-111">若要判斷呼叫端能夠修改的目錄物件屬性，請讀取物件的 **allowedAttributesEffective** 屬性。</span><span class="sxs-lookup"><span data-stu-id="17732-111">To determine the attributes of a directory object that the caller has the ability to modify, read the object's **allowedAttributesEffective** attribute.</span></span>

<span data-ttu-id="17732-112">如果呼叫端沒有足夠的許可權來修改屬性，可能會傳回下列傳回碼：</span><span class="sxs-lookup"><span data-stu-id="17732-112">If the caller does not have sufficient rights to modify a property, the following return codes may be returned:</span></span>

<span data-ttu-id="17732-113">E \_ ADS \_ 屬性 \_ 未 \_ 設定電子 \_ ADS \_ 屬性 \_ 未 \_ 修改</span><span class="sxs-lookup"><span data-stu-id="17732-113">E\_ADS\_PROPERTY\_NOT\_SET E\_ADS\_PROPERTY\_NOT\_MODIFIED</span></span>

 

 