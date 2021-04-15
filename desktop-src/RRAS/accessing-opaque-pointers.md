---
title: 存取不透明的指標
description: 用戶端可以使用不透明的指標來存取儲存在目的地的資訊。
ms.assetid: 1f6af84f-c6c9-4091-8e6b-2c773541ca97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a3435fd468b41c70105b0b239b35fe24212a7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507308"
---
# <a name="accessing-opaque-pointers"></a><span data-ttu-id="51ae8-103">存取不透明的指標</span><span class="sxs-lookup"><span data-stu-id="51ae8-103">Accessing Opaque Pointers</span></span>

<span data-ttu-id="51ae8-104">用戶端可以使用不透明的指標來存取儲存在目的地的資訊。</span><span class="sxs-lookup"><span data-stu-id="51ae8-104">Clients are able to access the information stored in destinations by using opaque pointers.</span></span> <span data-ttu-id="51ae8-105">若要使用此儲存體，用戶端必須先呼叫 [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) 來取得指標。</span><span class="sxs-lookup"><span data-stu-id="51ae8-105">To use the storage, the client must first call [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) to obtain the pointer.</span></span> <span data-ttu-id="51ae8-106">每當需要變更資訊時，用戶端必須先呼叫 [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) ，並將 *LockDest* 參數設為 **TRUE**，以鎖定目的地。</span><span class="sxs-lookup"><span data-stu-id="51ae8-106">Whenever a change to the information is necessary, the client must first lock the destination by calling [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) with the *LockDest* parameter set to **TRUE**.</span></span> <span data-ttu-id="51ae8-107">一旦鎖定目的地之後，用戶端就可以進行必要的變更。</span><span class="sxs-lookup"><span data-stu-id="51ae8-107">Once the destination is locked, the client can make the necessary change.</span></span> <span data-ttu-id="51ae8-108">您可以使用對 **RtmLockDestination** 的另一個呼叫來解除鎖定目的地，並將 *LockDest* 參數設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="51ae8-108">The destination can be unlocked using another call to **RtmLockDestination** with the *LockDest* parameter set to **FALSE**.</span></span>

<span data-ttu-id="51ae8-109">[**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination)函式也可讓用戶端使用 *獨佔* 參數，以使用讀取鎖定或寫入鎖定。</span><span class="sxs-lookup"><span data-stu-id="51ae8-109">The [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) function also allows a client to use either a read lock or a write lock, using the *Exclusive* parameter.</span></span> <span data-ttu-id="51ae8-110">用戶端只有在對使用不透明指標所保留的資訊進行變更時，才應該使用寫入鎖定。</span><span class="sxs-lookup"><span data-stu-id="51ae8-110">A client should use the write lock only when it is making changes to the information kept using the opaque pointer.</span></span> <span data-ttu-id="51ae8-111">用戶端可以使用讀取鎖定來查看儲存在目的地中的不透明指標資訊。</span><span class="sxs-lookup"><span data-stu-id="51ae8-111">Clients can use the read lock to view the opaque pointer information stored in a destination.</span></span>

<span data-ttu-id="51ae8-112">如需示範如何使用這些函數的範例程式碼，請參閱 [存取目的地中的不透明指標](access-the-opaque-pointer-in-a-destination.md)。</span><span class="sxs-lookup"><span data-stu-id="51ae8-112">For sample code that shows how to use these functions, see [Access the Opaque Pointer in a Destination](access-the-opaque-pointer-in-a-destination.md).</span></span>

 

 




