---
description: 您可以使用介面儲存任何種類的應用程式特定資料。 例如，代表遊戲中地圖的表面可能包含地形的相關資訊。
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: '私用介面資料 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66eabd8ce8b5cb93508d3ca8197970fb5d52d96a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991614"
---
# <a name="private-surface-data-direct3d-9"></a><span data-ttu-id="4583c-104">私用介面資料 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="4583c-104">Private Surface Data (Direct3D 9)</span></span>

<span data-ttu-id="4583c-105">您可以使用介面儲存任何種類的應用程式特定資料。</span><span class="sxs-lookup"><span data-stu-id="4583c-105">You can store any kind of application-specific data with a surface.</span></span> <span data-ttu-id="4583c-106">例如，代表遊戲中地圖的表面可能包含地形的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4583c-106">For example, a surface representing a map in a game might contain information about terrain.</span></span>

<span data-ttu-id="4583c-107">一個介面可以有一個以上的私用資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4583c-107">A surface can have more than one private data buffer.</span></span> <span data-ttu-id="4583c-108">每個緩衝區都是由您在將資料附加至介面時所提供的 GUID 所識別。</span><span class="sxs-lookup"><span data-stu-id="4583c-108">Each buffer is identified by a GUID that you supply when attaching the data to the surface.</span></span>

<span data-ttu-id="4583c-109">若要儲存私用表面資料，請使用 SetPrivateData，將指標傳遞至來源緩衝區、資料的大小，以及應用程式定義的資料 GUID。</span><span class="sxs-lookup"><span data-stu-id="4583c-109">To store private surface data, use SetPrivateData, passing a pointer to the source buffer, the size of the data, and an application-defined GUID for the data.</span></span> <span data-ttu-id="4583c-110">（選擇性）來源資料可以以 COM 物件的形式存在;在此情況下，您會將指標傳遞至物件的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面指標，並設定 D3DSPD \_ IUNKNOWNPOINTER 旗標。</span><span class="sxs-lookup"><span data-stu-id="4583c-110">Optionally, the source data can exist in the form of a COM object; in this case, you pass a pointer to the object's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface pointer and you set the D3DSPD\_IUNKNOWNPOINTER flag.</span></span>

<span data-ttu-id="4583c-111">SetPrivateData 會配置資料的內部緩衝區，並將其複製。</span><span class="sxs-lookup"><span data-stu-id="4583c-111">SetPrivateData allocates an internal buffer for the data and copies it.</span></span> <span data-ttu-id="4583c-112">然後您可以安全地釋放來源緩衝區或物件。</span><span class="sxs-lookup"><span data-stu-id="4583c-112">You can then safely free the source buffer or object.</span></span> <span data-ttu-id="4583c-113">呼叫 FreePrivateData 時，會釋放內部緩衝區或介面參考。</span><span class="sxs-lookup"><span data-stu-id="4583c-113">The internal buffer or interface reference is released when FreePrivateData is called.</span></span> <span data-ttu-id="4583c-114">這會在介面釋放時自動發生。</span><span class="sxs-lookup"><span data-stu-id="4583c-114">This happens automatically when the surface is freed.</span></span>

<span data-ttu-id="4583c-115">若要取得介面的私用資料，您必須配置正確大小的緩衝區，然後呼叫 GetPrivateData 方法，傳遞已指派給資料的 GUID。</span><span class="sxs-lookup"><span data-stu-id="4583c-115">To retrieve private data for a surface, you must allocate a buffer of the correct size and then call the GetPrivateData method, passing the GUID that was assigned to the data.</span></span> <span data-ttu-id="4583c-116">您必須負責釋放您用於此緩衝區的任何動態記憶體。</span><span class="sxs-lookup"><span data-stu-id="4583c-116">You are responsible for freeing any dynamic memory you use for this buffer.</span></span> <span data-ttu-id="4583c-117">如果資料是 COM 物件，這個方法會捕獲 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標。</span><span class="sxs-lookup"><span data-stu-id="4583c-117">If the data is a COM object, this method retrieves the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>

<span data-ttu-id="4583c-118">如果您不知道要配置的緩衝區有多大，請先在 pSizeOfData 中呼叫 GetPrivateData （零）。</span><span class="sxs-lookup"><span data-stu-id="4583c-118">If you don't know how big a buffer to allocate, first call GetPrivateData with zero in pSizeOfData.</span></span> <span data-ttu-id="4583c-119">如果方法因 D3DERR MOREDATA 而失敗 \_ ，則會傳回緩衝區所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="4583c-119">If the method fails with D3DERR\_MOREDATA, it returns the necessary number of bytes for the buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4583c-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="4583c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4583c-121">Direct3D 表面</span><span class="sxs-lookup"><span data-stu-id="4583c-121">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> </dl>

 

 
