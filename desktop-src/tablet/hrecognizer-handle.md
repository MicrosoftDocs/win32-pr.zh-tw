---
description: HRECOGNIZER 控制碼可用來建立辨識器內容、取出辨識器的屬性和屬性，以及判斷辨識器需要哪些封包屬性來執行辨識。
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: 'HRECOGNIZER 控制碼 (Recapis .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e78086ff86453ef8b0157bb3b274f3c47be0dc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318475"
---
# <a name="hrecognizer-handle"></a><span data-ttu-id="cf2e3-103">HRECOGNIZER 控制碼</span><span class="sxs-lookup"><span data-stu-id="cf2e3-103">HRECOGNIZER Handle</span></span>

<span data-ttu-id="cf2e3-104">**HRECOGNIZER** 控制碼可用來建立辨識器內容、取出辨識器的屬性和屬性，以及判斷辨識器需要哪些封包屬性來執行辨識。</span><span class="sxs-lookup"><span data-stu-id="cf2e3-104">An **HRECOGNIZER** handle is used to create a recognizer context, retrieve the recognizer's attributes and properties, and determine which packet properties the recognizer requires to perform recognition.</span></span>


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a><span data-ttu-id="cf2e3-105">備註</span><span class="sxs-lookup"><span data-stu-id="cf2e3-105">Remarks</span></span>

<span data-ttu-id="cf2e3-106">下列函數使用 **HRECOGNIZER**。</span><span class="sxs-lookup"><span data-stu-id="cf2e3-106">The following functions use an **HRECOGNIZER**.</span></span>



| <span data-ttu-id="cf2e3-107">函式</span><span class="sxs-lookup"><span data-stu-id="cf2e3-107">Function</span></span>                                                               | <span data-ttu-id="cf2e3-108">描述</span><span class="sxs-lookup"><span data-stu-id="cf2e3-108">Description</span></span>                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf2e3-109">**CreateRecognizer**</span><span class="sxs-lookup"><span data-stu-id="cf2e3-109">**CreateRecognizer**</span></span>](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | <span data-ttu-id="cf2e3-110">建立辨識器。</span><span class="sxs-lookup"><span data-stu-id="cf2e3-110">Creates a recognizer.</span></span><br/>                                                                   |
| [<span data-ttu-id="cf2e3-111">**DestroyRecognizer**</span><span class="sxs-lookup"><span data-stu-id="cf2e3-111">**DestroyRecognizer**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | <span data-ttu-id="cf2e3-112">終結辨識器。</span><span class="sxs-lookup"><span data-stu-id="cf2e3-112">Destroys a recognizer.</span></span><br/>                                                                  |
| [<span data-ttu-id="cf2e3-113">**GetRecoAttributes**</span><span class="sxs-lookup"><span data-stu-id="cf2e3-113">**GetRecoAttributes**</span></span>](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | <span data-ttu-id="cf2e3-114">傳回辨識器的屬性。</span><span class="sxs-lookup"><span data-stu-id="cf2e3-114">Returns the attributes of the recognizer.</span></span><br/>                                               |
| [<span data-ttu-id="cf2e3-115">**CreateCoNtext**</span><span class="sxs-lookup"><span data-stu-id="cf2e3-115">**CreateContext**</span></span>](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | <span data-ttu-id="cf2e3-116">建立辨識器內容。</span><span class="sxs-lookup"><span data-stu-id="cf2e3-116">Creates a recognizer context.</span></span><br/>                                                           |
| [<span data-ttu-id="cf2e3-117">**DestroyCoNtext**</span><span class="sxs-lookup"><span data-stu-id="cf2e3-117">**DestroyContext**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | <span data-ttu-id="cf2e3-118">終結辨識器內容。</span><span class="sxs-lookup"><span data-stu-id="cf2e3-118">Destroys a recognizer context.</span></span><br/>                                                          |
| [<span data-ttu-id="cf2e3-119">**GetAllRecognizers**</span><span class="sxs-lookup"><span data-stu-id="cf2e3-119">**GetAllRecognizers**</span></span>](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | <span data-ttu-id="cf2e3-120">取得所有辨識器。</span><span class="sxs-lookup"><span data-stu-id="cf2e3-120">Gets all recognizers.</span></span><br/>                                                                   |
| [<span data-ttu-id="cf2e3-121">**GetResultPropertyList**</span><span class="sxs-lookup"><span data-stu-id="cf2e3-121">**GetResultPropertyList**</span></span>](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | <span data-ttu-id="cf2e3-122">抓取辨識器可針對結果範圍傳回的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="cf2e3-122">Retrieves a list of properties the recognizer can return for a result range.</span></span><br/>            |
| [<span data-ttu-id="cf2e3-123">**GetPreferredPacketDescription**</span><span class="sxs-lookup"><span data-stu-id="cf2e3-123">**GetPreferredPacketDescription**</span></span>](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | <span data-ttu-id="cf2e3-124">抓取包含辨識器所使用之封包屬性的封包描述。</span><span class="sxs-lookup"><span data-stu-id="cf2e3-124">Retrieves a packet description that contains the packet properties the recognizer uses.</span></span><br/> |
| [<span data-ttu-id="cf2e3-125">**GetUnicodeRanges**</span><span class="sxs-lookup"><span data-stu-id="cf2e3-125">**GetUnicodeRanges**</span></span>](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | <span data-ttu-id="cf2e3-126">抓取辨識器支援的 Unicode 點範圍。</span><span class="sxs-lookup"><span data-stu-id="cf2e3-126">Retrieves the ranges of Unicode points that the recognizer supports.</span></span><br/>                    |
| [<span data-ttu-id="cf2e3-127">**LoadCachedAttributes**</span><span class="sxs-lookup"><span data-stu-id="cf2e3-127">**LoadCachedAttributes**</span></span>](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | <span data-ttu-id="cf2e3-128">載入辨識器的快取屬性。</span><span class="sxs-lookup"><span data-stu-id="cf2e3-128">Loads the cached attributes of a recognizer.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="cf2e3-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf2e3-129">Requirements</span></span>



| <span data-ttu-id="cf2e3-130">需求</span><span class="sxs-lookup"><span data-stu-id="cf2e3-130">Requirement</span></span> | <span data-ttu-id="cf2e3-131">值</span><span class="sxs-lookup"><span data-stu-id="cf2e3-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cf2e3-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf2e3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cf2e3-133">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf2e3-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="cf2e3-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf2e3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cf2e3-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="cf2e3-135">None supported</span></span><br/>                                                            |
| <span data-ttu-id="cf2e3-136">標頭</span><span class="sxs-lookup"><span data-stu-id="cf2e3-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf2e3-137"><dt>Recapis。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf2e3-137"><dt>Recapis.h</dt></span></span> </dl> |



 

 




