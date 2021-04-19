---
description: 位址篩選器會通知網路監視器驅動程式，接受具有其中一種指定 MAC 網址類別型的框架 (乙太網路、權杖響鈴和 FDDI) 。
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: 寫入 ADDRESSTABLE 篩選部分
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b06b00d046d555dffc39561b817629f4f47ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978364"
---
# <a name="writing-addresstable-filter-portion"></a><span data-ttu-id="42039-103">寫入 ADDRESSTABLE 篩選部分</span><span class="sxs-lookup"><span data-stu-id="42039-103">Writing ADDRESSTABLE Filter Portion</span></span>

<span data-ttu-id="42039-104">位址篩選器會通知網路監視器驅動程式，接受具有其中一種指定 MAC 網址類別型的框架 (乙太網路、權杖響鈴和 FDDI) 。</span><span class="sxs-lookup"><span data-stu-id="42039-104">The address filter notifies the Network Monitor driver to accept frames that have one of a variety of specified MAC address types (Ethernet, Token Ring, and FDDI).</span></span> <span data-ttu-id="42039-105">您可以指定最多8個位址配對。</span><span class="sxs-lookup"><span data-stu-id="42039-105">You can specify a maximum of eight address pairs.</span></span> <span data-ttu-id="42039-106">位址組可以指定來源、目的地、兩者或兩者皆非。</span><span class="sxs-lookup"><span data-stu-id="42039-106">An address pair can specify a source, a destination, both, or neither.</span></span>

<span data-ttu-id="42039-107">篩選器的位址部分是由兩個結構所組成： [**ADDRESSTABLE**](addresstable.md) 和 [**ADDRESSPAIR**](addresspair.md)。</span><span class="sxs-lookup"><span data-stu-id="42039-107">The address portion of the filter consists of two structures: [**ADDRESSTABLE**](addresstable.md) and [**ADDRESSPAIR**](addresspair.md).</span></span>

<span data-ttu-id="42039-108">如果您沒有指定位址，則所有畫面格都會通過位址篩選。</span><span class="sxs-lookup"><span data-stu-id="42039-108">If you specify NO addresses, then ALL frames will pass the address filter.</span></span> <span data-ttu-id="42039-109">但是，如果您指定任何位址，則只有通過指定位址篩選的框架才會通過。</span><span class="sxs-lookup"><span data-stu-id="42039-109">However, if you specify any addresses, only those frames that pass the given address filter will pass.</span></span>

<span data-ttu-id="42039-110">建立位址篩選牽涉到配置 [**ADDRESSTABLE**](addresstable.md) 結構，以及填入 [**ADDRESSPAIR**](addresspair.md) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="42039-110">Building the address filter involves allocating an [**ADDRESSTABLE**](addresstable.md) structure and filling in members of the [**ADDRESSPAIR**](addresspair.md) structure.</span></span>

<span data-ttu-id="42039-111">**若要建立 capture 篩選器的位址部分**</span><span class="sxs-lookup"><span data-stu-id="42039-111">**To build the address portion of a capture filter**</span></span>

1.  <span data-ttu-id="42039-112">使用 [**CAPTUREFILTER**](capturefilter.md)結構的 **CAPTUREFILTER \_ 旗標 \_ 本機 \_ 旗標**，將捕捉限制在本機電腦的進出流量。</span><span class="sxs-lookup"><span data-stu-id="42039-112">Use the **CAPTUREFILTER\_FLAGS\_LOCAL\_ONLY** flag of the [**CAPTUREFILTER**](capturefilter.md) structure to restrict the capture to traffic to and from your local computer.</span></span>

    <span data-ttu-id="42039-113">設定此旗標不會將 NIC 設定為混合模式;capture 檔案只會捕獲本機流量。</span><span class="sxs-lookup"><span data-stu-id="42039-113">Setting this flag will not set the NIC to promiscuous mode; the capture file will capture only local traffic.</span></span>

2.  <span data-ttu-id="42039-114">使用下列範例程式碼來定義 [**ADDRESSTABLE**](addresstable.md) 結構：</span><span class="sxs-lookup"><span data-stu-id="42039-114">Use the following example code to define the [**ADDRESSTABLE**](addresstable.md) structure:</span></span>

    ``` syntax
    typedef struct _ADDRESSTABLE
    {
        DWORD           nAddressPairs;
        DWORD           nNonMacAddressPairs;
        ADDRESSPAIR     AddressPair[MAX_ADDRESS_PAIRS];
    } ADDRESSTABLE;

    typedef ADDRESSTABLE *LPADDRESSTABLE;
     
    typedef struct _ADDRESSPAIR
    {
        WORD        AddressFlags;
        WORD        NalReserved;
        ADDRESS     DstAddress;
        ADDRESS     SrcAddress;
    } ADDRESSPAIR;

    typedef ADDRESSPAIR *LPADDRESSPAIR;
    ```

3.  <span data-ttu-id="42039-115">使用下表所列的資訊，來選取 [**ADDRESSPAIR**](addresspair.md) 旗標類型。</span><span class="sxs-lookup"><span data-stu-id="42039-115">Use the information, listed in the following table, to select an [**ADDRESSPAIR**](addresspair.md) flag type.</span></span> 

    | <span data-ttu-id="42039-116">旗標</span><span class="sxs-lookup"><span data-stu-id="42039-116">Flag</span></span>                             | <span data-ttu-id="42039-117">意義</span><span class="sxs-lookup"><span data-stu-id="42039-117">Meaning</span></span>                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | <span data-ttu-id="42039-118">位址 \_ 旗標 \_ 符合 \_ DST</span><span class="sxs-lookup"><span data-stu-id="42039-118">ADDRESS\_FLAGS\_MATCH\_DST</span></span>       | <span data-ttu-id="42039-119">符合目的地位址。</span><span class="sxs-lookup"><span data-stu-id="42039-119">Matches a destination address.</span></span>                                                        |
    | <span data-ttu-id="42039-120">位址 \_ 旗標 \_ 符合 \_ SRC</span><span class="sxs-lookup"><span data-stu-id="42039-120">ADDRESS\_FLAGS\_MATCH\_SRC</span></span>       | <span data-ttu-id="42039-121">符合來源位址</span><span class="sxs-lookup"><span data-stu-id="42039-121">Matches a source address</span></span>                                                              |
    | <span data-ttu-id="42039-122">位址 \_ 旗標 \_ 排除</span><span class="sxs-lookup"><span data-stu-id="42039-122">ADDRESS\_FLAGS\_EXCLUDE</span></span>          | <span data-ttu-id="42039-123">如果找到此位址 (定義的來源或目的地) ，則排除框架。</span><span class="sxs-lookup"><span data-stu-id="42039-123">Excludes the frame if this address is found (either a defined source or destination).</span></span> |
    | <span data-ttu-id="42039-124">位址 \_ 旗標 \_ DST \_ 群組 \_ 位址</span><span class="sxs-lookup"><span data-stu-id="42039-124">ADDRESS\_FLAGS\_DST\_GROUP\_ADDR</span></span> | <span data-ttu-id="42039-125">比對目的地位址的群組位 (，) 只適用于廣播類型的訊息。</span><span class="sxs-lookup"><span data-stu-id="42039-125">Matches group bit (of the destination address) only for broadcast-type messages.</span></span>      |
    | <span data-ttu-id="42039-126">\_ \_ 符合兩者的位址旗標 \_</span><span class="sxs-lookup"><span data-stu-id="42039-126">ADDRESS\_FLAGS\_MATCH\_BOTH</span></span>      | <span data-ttu-id="42039-127">符合目的地和來源位址。</span><span class="sxs-lookup"><span data-stu-id="42039-127">Matches both the destination and source addresses.</span></span>                                    |

    

     

4.  <span data-ttu-id="42039-128">填入目的地位址，該位址會針對您選取的 [**ADDRESSPAIR**](addresspair.md) 旗標進行評估。</span><span class="sxs-lookup"><span data-stu-id="42039-128">Fill in a destination address, which is evaluated against the [**ADDRESSPAIR**](addresspair.md) flag that you select.</span></span>
5.  <span data-ttu-id="42039-129">填入來源位址，該位址會針對您選取的 [**ADDRESSPAIR**](addresspair.md) 旗標進行評估。</span><span class="sxs-lookup"><span data-stu-id="42039-129">Fill in a source address, which is evaluated against the [**ADDRESSPAIR**](addresspair.md) flag that you select.</span></span>
6.  <span data-ttu-id="42039-130">以 [**ADDRESSPAIR**](addresspair.md)結構的陣列填入 [**ADDRESSTABLE**](addresstable.md)結構，其中包含驅動程式所評估的位址組。</span><span class="sxs-lookup"><span data-stu-id="42039-130">Populate the [**ADDRESSTABLE**](addresstable.md) structure with an array of [**ADDRESSPAIR**](addresspair.md) structures, which includes the address pairs that the driver evaluates.</span></span> <span data-ttu-id="42039-131">所有位址組都會評估為邏輯 OR 語句 (ADDRESSPAIR 1 \| \| ADDRESSPAIR 2) 。</span><span class="sxs-lookup"><span data-stu-id="42039-131">All address pairs are evaluated as a logical OR statement (ADDRESSPAIR 1 \|\| ADDRESSPAIR 2).</span></span> <span data-ttu-id="42039-132">您最多可以在捕獲篩選中包含八個位址組。</span><span class="sxs-lookup"><span data-stu-id="42039-132">You can include a maximum of eight address pairs in a capture filter.</span></span>

 

 



