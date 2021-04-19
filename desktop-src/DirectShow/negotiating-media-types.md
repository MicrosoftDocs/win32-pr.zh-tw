---
description: 協商媒體類型
ms.assetid: 9872128c-4e3d-4ac8-afc4-b3dc516a0925
title: 協商媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdcb78cfef6b8396d866ea148267c5a899cd353
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986023"
---
# <a name="negotiating-media-types"></a><span data-ttu-id="88956-103">協商媒體類型</span><span class="sxs-lookup"><span data-stu-id="88956-103">Negotiating Media Types</span></span>

<span data-ttu-id="88956-104">當篩選圖形管理員呼叫 [**IPin：： Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) 方法時，會有數個選項可用於指定媒體類型：</span><span class="sxs-lookup"><span data-stu-id="88956-104">When the Filter Graph Manager calls the [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method, it has several options for specifying a media type:</span></span>

-   <span data-ttu-id="88956-105">**完成類型：** 如果媒體類型是完全指定的，則會嘗試使用該類型連接。</span><span class="sxs-lookup"><span data-stu-id="88956-105">**Complete type:** If the media type is fully specified, the pins attempt to connect with that type.</span></span> <span data-ttu-id="88956-106">如果無法連線，連接嘗試就會失敗。</span><span class="sxs-lookup"><span data-stu-id="88956-106">If they cannot, the connection attempt fails.</span></span>
-   <span data-ttu-id="88956-107">**部分媒體類型：** 如果主要類型、子類型或格式類型為 GUID Null，則媒體類型為 [ *部分* ] \_ 。</span><span class="sxs-lookup"><span data-stu-id="88956-107">**Partial media type:** A media type is *partial* if the major type, subtype, or format type is GUID\_NULL.</span></span> <span data-ttu-id="88956-108">值 GUID \_ Null 可做為 "萬用字元"，表示可接受任何值。</span><span class="sxs-lookup"><span data-stu-id="88956-108">The value GUID\_NULL acts as a "wildcard," indicating that any value is acceptable.</span></span> <span data-ttu-id="88956-109">Pin 會協商與部分類型一致的型別。</span><span class="sxs-lookup"><span data-stu-id="88956-109">The pins negotiate a type that is consistent with the partial type.</span></span>
-   <span data-ttu-id="88956-110">**沒有媒體類型：** 如果篩選圖形管理員傳遞 **Null** 指標，則 pin 可以接受兩個 pin 都可接受的任何媒體類型。</span><span class="sxs-lookup"><span data-stu-id="88956-110">**No media type:** If the Filter Graph Manager passes a **NULL** pointer, the pins can agree to any media type that is acceptable to both pins.</span></span>

<span data-ttu-id="88956-111">如果釘選連線，連接一定會有完整的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="88956-111">If the pins do connect, the connection always has a complete media type.</span></span> <span data-ttu-id="88956-112">篩選圖形管理員所提供之媒體類型的目的是要限制可能的連線類型。</span><span class="sxs-lookup"><span data-stu-id="88956-112">The purpose of the media type given by the Filter Graph Manager is to limit the possible connection types.</span></span>

<span data-ttu-id="88956-113">在進行協調程式期間，輸出 pin 會藉由呼叫輸入 pin 的 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 方法來提議媒體類型。</span><span class="sxs-lookup"><span data-stu-id="88956-113">During the negotiation process, the output pin proposes a media type by calling the input pin's [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span> <span data-ttu-id="88956-114">輸入 pin 可以接受或拒絕建議的類型。</span><span class="sxs-lookup"><span data-stu-id="88956-114">The input pin can accept or reject the proposed type.</span></span> <span data-ttu-id="88956-115">此程式會重複，直到輸入的 pin 接受型別，或是輸出的釘選出型別且連接失敗。</span><span class="sxs-lookup"><span data-stu-id="88956-115">This process repeats until either the input pin accepts a type, or the output pin runs out of types and the connection fails.</span></span>

<span data-ttu-id="88956-116">輸出圖釘如何選取要建議的媒體類型取決於執行。</span><span class="sxs-lookup"><span data-stu-id="88956-116">How an output pin selects media types to propose depends on the implementation.</span></span> <span data-ttu-id="88956-117">在 DirectShow 基類中，輸出圖釘會在輸入 pin 上呼叫 [**IPin：： EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) 。</span><span class="sxs-lookup"><span data-stu-id="88956-117">In the DirectShow base classes, the output pin calls [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) on the input pin.</span></span> <span data-ttu-id="88956-118">這個方法會傳回列舉輸入釘選媒體類型的列舉值。</span><span class="sxs-lookup"><span data-stu-id="88956-118">This method returns an enumerator that enumerates the input pin's preferred media types.</span></span> <span data-ttu-id="88956-119">如果失敗，輸出釘會列舉自己慣用的類型。</span><span class="sxs-lookup"><span data-stu-id="88956-119">Failing that, the output pin enumerates its own preferred types.</span></span>

<span data-ttu-id="88956-120">**使用媒體類型**</span><span class="sxs-lookup"><span data-stu-id="88956-120">**Working with Media Types**</span></span>

<span data-ttu-id="88956-121">在接收 **AM \_ 媒體 \_ 類型** 參數的任何函式中，一律先驗證 **cbFormat** 和 **formattype** 的值，再取值 **pbFormat** 成員。</span><span class="sxs-lookup"><span data-stu-id="88956-121">In any function that receives an **AM\_MEDIA\_TYPE** parameter, always validate the values of **cbFormat** and **formattype** before dereferencing the **pbFormat** member.</span></span> <span data-ttu-id="88956-122">下列程式碼不正確：</span><span class="sxs-lookup"><span data-stu-id="88956-122">The following code is incorrect:</span></span>


```C++
if (pmt->formattype == FORMAT_VideoInfo)
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Wrong!
}
```



<span data-ttu-id="88956-123">下列程式碼是正確的：</span><span class="sxs-lookup"><span data-stu-id="88956-123">The following code is correct:</span></span>


```C++
if ((pmt->formattype == FORMAT_VideoInfo) && 
    (pmt->cbFormat > sizeof(VIDEOINFOHEADER) &&
    (pbFormat != NULL))
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Now you can dereference pVIH.
}
```



 

 



