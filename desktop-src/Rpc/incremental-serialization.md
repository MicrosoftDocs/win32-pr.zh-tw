---
title: 累加式序列化
description: 當使用累加樣式序列化時，您會提供三個常式來操作緩衝區。
ms.assetid: c7383b4d-94d1-4edd-ac29-c11fb5343156
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409f8da0881719ec9273f4dd12cc99e3d36c35a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507401"
---
# <a name="incremental-serialization"></a><span data-ttu-id="1af48-103">累加式序列化</span><span class="sxs-lookup"><span data-stu-id="1af48-103">Incremental Serialization</span></span>

<span data-ttu-id="1af48-104">當使用累加樣式序列化時，您會提供三個常式來操作緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1af48-104">When using the incremental style serialization, you supply three routines to manipulate the buffer.</span></span> <span data-ttu-id="1af48-105">這些常式包括：配置、讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="1af48-105">These routines are: Alloc, Read, and Write.</span></span> <span data-ttu-id="1af48-106">配置常式會配置所需大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1af48-106">The Alloc routine allocates a buffer of the required size.</span></span> <span data-ttu-id="1af48-107">寫入常式會將資料寫入緩衝區，而讀取常式會抓取包含已封送資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1af48-107">The Write routine writes the data into the buffer, and the Read routine retrieves a buffer that contains marshaled data.</span></span> <span data-ttu-id="1af48-108">單一序列化呼叫可以對這些常式進行數個呼叫。</span><span class="sxs-lookup"><span data-stu-id="1af48-108">A single serialization call can make several calls to these routines.</span></span>

<span data-ttu-id="1af48-109">序列化的遞增樣式使用下列常式：</span><span class="sxs-lookup"><span data-stu-id="1af48-109">The incremental style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="1af48-110">**MesEncodeIncrementalHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="1af48-110">**MesEncodeIncrementalHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)
-   [<span data-ttu-id="1af48-111">**MesDecodeIncrementalHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="1af48-111">**MesDecodeIncrementalHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [<span data-ttu-id="1af48-112">**MesIncrementalHandleReset**</span><span class="sxs-lookup"><span data-stu-id="1af48-112">**MesIncrementalHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)
-   [<span data-ttu-id="1af48-113">**MesHandleFree**</span><span class="sxs-lookup"><span data-stu-id="1af48-113">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="1af48-114">您必須提供之配置、讀取和寫入函式的原型如下所示：</span><span class="sxs-lookup"><span data-stu-id="1af48-114">The prototypes for the Alloc, Read, and Write functions that you must provide are shown below:</span></span>

``` syntax
void __RPC_USER Alloc (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returns pointer to allocated buffer */
   unsigned int *pSize); /* inputs requested bytes; outputs 
                         /* pBuffer size */

void __RPC_USER Write (
   void *State,          /* application-defined pointer */
   char *Buffer,         /* buffer with serialized data */
   unsigned int Size);   /* number of bytes to write from Buffer */

void __RPC_USER Read (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returned pointer to buffer with data */
   unsigned int *pSize); /* number of bytes to read into pBuffer */
```

<span data-ttu-id="1af48-115">所有三個函式的狀態輸入參數都是與編碼服務控制碼相關聯的應用程式定義指標。</span><span class="sxs-lookup"><span data-stu-id="1af48-115">The State input a parameter for all three functions is the application-defined pointer that was associated with the encoding services handle.</span></span> <span data-ttu-id="1af48-116">應用程式可以使用這個指標來存取包含應用程式特定資訊的結構，例如，檔案控制代碼或資料流程指標。</span><span class="sxs-lookup"><span data-stu-id="1af48-116">The application can use this pointer to access the structure containing application-specific information, such as a file handle or stream pointer.</span></span> <span data-ttu-id="1af48-117">請注意，除了傳遞給配置、讀取和寫入函式以外，存根不會修改狀態指標。</span><span class="sxs-lookup"><span data-stu-id="1af48-117">Note that the stubs do not modify the State pointer other than to pass it to the Alloc, Read, and Write functions.</span></span> <span data-ttu-id="1af48-118">在編碼期間，會呼叫配置以取得資料已序列化的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1af48-118">During encoding, Alloc is called to obtain a buffer into which the data is serialized.</span></span> <span data-ttu-id="1af48-119">然後，會呼叫 Write 來讓應用程式控制序列化資料的儲存時間和位置。</span><span class="sxs-lookup"><span data-stu-id="1af48-119">Then, Write is called to enable the application to control when and where the serialized data is stored.</span></span> <span data-ttu-id="1af48-120">在解碼期間，會呼叫 Read 來傳回所要求的序列化資料位元組數目，從應用程式儲存的位置。</span><span class="sxs-lookup"><span data-stu-id="1af48-120">During decoding, Read is called to return the requested number of bytes of serialized data from where the application stored it.</span></span>

<span data-ttu-id="1af48-121">累加樣式的一項重要功能是，控制碼會為您保持狀態指標。</span><span class="sxs-lookup"><span data-stu-id="1af48-121">An important feature of the incremental style is that the handle keeps the state pointer for you.</span></span> <span data-ttu-id="1af48-122">除了將指標傳遞至配置、寫入或讀取函式時，此指標會維持狀態，而且 RPC 函式永遠不會觸及這些函數。</span><span class="sxs-lookup"><span data-stu-id="1af48-122">This pointer maintains the state and is never touched by the RPC functions, except when passing the pointer to Alloc, Write, or Read function.</span></span> <span data-ttu-id="1af48-123">此控制碼也會維護內部狀態，讓您可以視需要新增填補來將數個型別實例編碼和解碼成相同的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1af48-123">The handle also maintains an internal state that makes it possible to encode and decode several type instances to the same buffer by adding padding as needed for alignment.</span></span> <span data-ttu-id="1af48-124">[**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)函式會將控制碼重設為其初始狀態，以啟用從緩衝區開頭讀取或寫入的功能。</span><span class="sxs-lookup"><span data-stu-id="1af48-124">The [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) function resets a handle to its initial state to enable reading or writing from the beginning of the buffer.</span></span>

<span data-ttu-id="1af48-125">配置和寫入函式，以及應用程式定義的指標，會透過呼叫 [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) 函式與編碼服務控制碼相關聯。</span><span class="sxs-lookup"><span data-stu-id="1af48-125">The Alloc and Write functions, along with an application-defined pointer, are associated with an encoding-services handle by a call to the [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) function.</span></span> <span data-ttu-id="1af48-126">**MesEncodeIncrementalHandleCreate** 會配置控制碼所需的記憶體，然後將它初始化。</span><span class="sxs-lookup"><span data-stu-id="1af48-126">**MesEncodeIncrementalHandleCreate** allocates the memory needed for the handle and then initializes it.</span></span>

<span data-ttu-id="1af48-127">應用程式可以呼叫 [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) 來建立解碼控制碼、 [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) 重新初始化控制碼，或使用 [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) 來釋放控制碼的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1af48-127">The application can call [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) to create a decoding handle, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) to reinitialize the handle, or [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="1af48-128">Read 函式和應用程式定義的參數，會透過呼叫 **MesDecodeIncrementalHandleCreate** 常式來與解碼控制碼相關聯。</span><span class="sxs-lookup"><span data-stu-id="1af48-128">The Read function, along with an application-defined parameter, is associated with a decoding handle by a call to the **MesDecodeIncrementalHandleCreate** routine.</span></span> <span data-ttu-id="1af48-129">函式會建立控制碼，並將其初始化。</span><span class="sxs-lookup"><span data-stu-id="1af48-129">The function creates the handle and initializes it.</span></span>

<span data-ttu-id="1af48-130">[**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)的 UserState、配置、寫入和讀取參數可以是 **Null** ，表示沒有任何變更。</span><span class="sxs-lookup"><span data-stu-id="1af48-130">The UserState, Alloc, Write, and Read parameters of [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) can be **NULL** to indicate no change.</span></span>

 

 




