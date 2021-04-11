---
description: 包含在開始時描述專家的資料。
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: 'EXPERTSTARTUPINFO 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTARTUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 627d47cec09a683f80c16374561899ab008d0596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936635"
---
# <a name="expertstartupinfo-structure"></a><span data-ttu-id="25f7a-103">EXPERTSTARTUPINFO 結構</span><span class="sxs-lookup"><span data-stu-id="25f7a-103">EXPERTSTARTUPINFO structure</span></span>

<span data-ttu-id="25f7a-104">**EXPERTSTARTUPINFO** 結構包含的資料會在開始時描述專家。</span><span class="sxs-lookup"><span data-stu-id="25f7a-104">The **EXPERTSTARTUPINFO** structure contains data that describes an expert when it starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="25f7a-105">語法</span><span class="sxs-lookup"><span data-stu-id="25f7a-105">Syntax</span></span>


```C++
typedef struct _EXPERTSTARTUPINFO {
  DWORD          Flags;
  HCAPTURE       hCapture;
  char           szCaptureFile[MAX_PATH];
  DWORD          dwFrameNumber;
  HPROTOCOL      hProtocol;
  LPPROPERTYINST lpPropertyInst;
  struct {
    BYTE BitNumber;
    BOOL bOn;
  } sBitfield;
} EXPERTSTARTUPINFO, *PEXPERTSTARTUPINFO;
```



## <a name="members"></a><span data-ttu-id="25f7a-106">成員</span><span class="sxs-lookup"><span data-stu-id="25f7a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="25f7a-107">**旗標**</span><span class="sxs-lookup"><span data-stu-id="25f7a-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="25f7a-108">描述專家的旗標。</span><span class="sxs-lookup"><span data-stu-id="25f7a-108">Flags that describe the expert.</span></span>

</dd> <dt>

<span data-ttu-id="25f7a-109">**hCapture**</span><span class="sxs-lookup"><span data-stu-id="25f7a-109">**hCapture**</span></span>
</dt> <dd>

<span data-ttu-id="25f7a-110">捕捉的控制碼。</span><span class="sxs-lookup"><span data-stu-id="25f7a-110">Handle to a capture.</span></span>

</dd> <dt>

<span data-ttu-id="25f7a-111">**szCaptureFile**</span><span class="sxs-lookup"><span data-stu-id="25f7a-111">**szCaptureFile**</span></span>
</dt> <dd>

<span data-ttu-id="25f7a-112">Capture 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="25f7a-112">Name of the capture file.</span></span>

</dd> <dt>

<span data-ttu-id="25f7a-113">**dwFrameNumber**</span><span class="sxs-lookup"><span data-stu-id="25f7a-113">**dwFrameNumber**</span></span>
</dt> <dd>

<span data-ttu-id="25f7a-114">畫面格編號。</span><span class="sxs-lookup"><span data-stu-id="25f7a-114">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="25f7a-115">**hProtocol**</span><span class="sxs-lookup"><span data-stu-id="25f7a-115">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="25f7a-116">通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="25f7a-116">Handle to the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="25f7a-117">**lpPropertyInst**</span><span class="sxs-lookup"><span data-stu-id="25f7a-117">**lpPropertyInst**</span></span>
</dt> <dd>

<span data-ttu-id="25f7a-118">[**PROPERTYINST**](propertyinst.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="25f7a-118">Pointer to a [**PROPERTYINST**](propertyinst.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="25f7a-119">**sBitfield**</span><span class="sxs-lookup"><span data-stu-id="25f7a-119">**sBitfield**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f7a-120">**BitNumber**</span><span class="sxs-lookup"><span data-stu-id="25f7a-120">**BitNumber**</span></span>
</dt> <dd>

<span data-ttu-id="25f7a-121">只有在 [**PROPERTYINST**](propertyinst.md)結構的 **DataQualifier** 成員設定為 [ \_ QUAL] 旗標時，才會使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="25f7a-121">Used only if the **DataQualifier** member of the [**PROPERTYINST**](propertyinst.md) structure is set to PROP\_QUAL\_FLAGS.</span></span>

</dd> <dt>

<span data-ttu-id="25f7a-122">**邦**</span><span class="sxs-lookup"><span data-stu-id="25f7a-122">**bOn**</span></span>
</dt> <dd>

<span data-ttu-id="25f7a-123">只有在 [**PROPERTYINST**](propertyinst.md)結構的 **DataQualifier** 成員設定為 [ \_ QUAL] 旗標時，才會使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="25f7a-123">Used only if the **DataQualifier** member of the [**PROPERTYINST**](propertyinst.md) structure is set to PROP\_QUAL\_FLAGS.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25f7a-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="25f7a-124">Requirements</span></span>



| <span data-ttu-id="25f7a-125">需求</span><span class="sxs-lookup"><span data-stu-id="25f7a-125">Requirement</span></span> | <span data-ttu-id="25f7a-126">值</span><span class="sxs-lookup"><span data-stu-id="25f7a-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="25f7a-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="25f7a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="25f7a-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25f7a-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="25f7a-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="25f7a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="25f7a-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25f7a-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="25f7a-131">標頭</span><span class="sxs-lookup"><span data-stu-id="25f7a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="25f7a-132"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="25f7a-132"><dt>Netmon.h</dt></span></span> </dl> |



 

 




