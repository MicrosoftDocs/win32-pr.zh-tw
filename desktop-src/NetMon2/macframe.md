---
description: MACFRAME 結構是最常見初始通訊協定的聯集。
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: 'MACFRAME 聯集 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MACFRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a7901daf467a63586543c52ca8a214d5d0094982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973865"
---
# <a name="macframe-union"></a><span data-ttu-id="3b157-103">MACFRAME 聯集</span><span class="sxs-lookup"><span data-stu-id="3b157-103">MACFRAME union</span></span>

<span data-ttu-id="3b157-104">**MACFRAME** 結構是最常見初始通訊協定的聯集。</span><span class="sxs-lookup"><span data-stu-id="3b157-104">The **MACFRAME** structure is a union of the most common initial protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b157-105">語法</span><span class="sxs-lookup"><span data-stu-id="3b157-105">Syntax</span></span>


```C++
typedef union {
  LPBYTE      MacHeader;
  LPETHERNET  Ethernet;
  LPTOKENRING Tokenring;
  LPFDDI      Fddi;
} MACFRAME, *LPMACFRAME;
```



## <a name="members"></a><span data-ttu-id="3b157-106">成員</span><span class="sxs-lookup"><span data-stu-id="3b157-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3b157-107">**MacHeader**</span><span class="sxs-lookup"><span data-stu-id="3b157-107">**MacHeader**</span></span>
</dt> <dd>

<span data-ttu-id="3b157-108">框架的泛型指標。</span><span class="sxs-lookup"><span data-stu-id="3b157-108">Generic pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="3b157-109">**乙太網路**</span><span class="sxs-lookup"><span data-stu-id="3b157-109">**Ethernet**</span></span>
</dt> <dd>

<span data-ttu-id="3b157-110">框架的乙太網路指標。</span><span class="sxs-lookup"><span data-stu-id="3b157-110">Ethernet pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="3b157-111">**Tokenring**</span><span class="sxs-lookup"><span data-stu-id="3b157-111">**Tokenring**</span></span>
</dt> <dd>

<span data-ttu-id="3b157-112">框架的 Token 環形指標。</span><span class="sxs-lookup"><span data-stu-id="3b157-112">Token ring pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="3b157-113">**Fddi**</span><span class="sxs-lookup"><span data-stu-id="3b157-113">**Fddi**</span></span>
</dt> <dd>

<span data-ttu-id="3b157-114">畫面格的 FDDI 指標。</span><span class="sxs-lookup"><span data-stu-id="3b157-114">FDDI pointer to a frame.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b157-115">備註</span><span class="sxs-lookup"><span data-stu-id="3b157-115">Remarks</span></span>

<span data-ttu-id="3b157-116">此結構最常用來做為重迭。</span><span class="sxs-lookup"><span data-stu-id="3b157-116">This structure is most frequently used as an overlay.</span></span> <span data-ttu-id="3b157-117">若要讓第一個通訊協定的屬性可供存取，請將框架轉換成與通訊協定相同的類型。</span><span class="sxs-lookup"><span data-stu-id="3b157-117">To make the properties of the first protocol accessible, cast the frame as the same type as the protocol.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b157-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b157-118">Requirements</span></span>



| <span data-ttu-id="3b157-119">需求</span><span class="sxs-lookup"><span data-stu-id="3b157-119">Requirement</span></span> | <span data-ttu-id="3b157-120">值</span><span class="sxs-lookup"><span data-stu-id="3b157-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3b157-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b157-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3b157-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b157-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3b157-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b157-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3b157-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b157-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3b157-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3b157-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b157-126"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="3b157-126"><dt>Netmon.h</dt></span></span> </dl> |



 

 




