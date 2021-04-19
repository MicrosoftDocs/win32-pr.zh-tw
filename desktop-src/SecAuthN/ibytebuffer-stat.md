---
description: Stat 方法會從資料流程物件中捕獲統計資訊。
ms.assetid: 7dfb59e9-143a-402e-990a-a2b35e6443dd
title: 'IByteBuffer：： Stat 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Stat
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bbbf033fc9ad5a25b3bcf5c22028ac1237f46c14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985323"
---
# <a name="ibytebufferstat-method"></a><span data-ttu-id="4cbaf-103">IByteBuffer：： Stat 方法</span><span class="sxs-lookup"><span data-stu-id="4cbaf-103">IByteBuffer::Stat method</span></span>

<span data-ttu-id="4cbaf-104">\[**Stat** 方法可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="4cbaf-104">\[The **Stat** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4cbaf-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="4cbaf-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4cbaf-106">[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="4cbaf-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="4cbaf-107">**Stat** 方法會從資料流程物件中捕獲統計資訊。</span><span class="sxs-lookup"><span data-stu-id="4cbaf-107">The **Stat** method retrieves statistical information from the stream object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cbaf-108">語法</span><span class="sxs-lookup"><span data-stu-id="4cbaf-108">Syntax</span></span>


```C++
HRESULT Stat(
  [out] LPSTATSTRUCT pstatstg,
  [in]  LONG         grfStatFlag
);
```



## <a name="parameters"></a><span data-ttu-id="4cbaf-109">參數</span><span class="sxs-lookup"><span data-stu-id="4cbaf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cbaf-110">*pstatstg* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4cbaf-110">*pstatstg* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cbaf-111">指向 **STATSTRUCT** 結構，這個方法會在其中放置此資料流程物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4cbaf-111">Points to a **STATSTRUCT** structure where this method places information about this stream object.</span></span> <span data-ttu-id="4cbaf-112">如果發生錯誤，此指標會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="4cbaf-112">This pointer is **NULL** if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="4cbaf-113">*grfStatFlag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4cbaf-113">*grfStatFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cbaf-114">指定此方法不會傳回 **STATSTRUCT** 結構中的某些欄位，因此會儲存記憶體配置作業。</span><span class="sxs-lookup"><span data-stu-id="4cbaf-114">Specifies that this method does not return some of the fields in the **STATSTRUCT** structure, thus saving a memory allocation operation.</span></span> <span data-ttu-id="4cbaf-115">值取自 [**STATFLAG**](/windows/win32/api/wtypes/ne-wtypes-statflag) 列舉</span><span class="sxs-lookup"><span data-stu-id="4cbaf-115">Values are taken from the [**STATFLAG**](/windows/win32/api/wtypes/ne-wtypes-statflag) enumeration</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cbaf-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="4cbaf-116">Return value</span></span>

<span data-ttu-id="4cbaf-117">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="4cbaf-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="4cbaf-118">值為 S \_ OK 表示呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="4cbaf-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cbaf-119">備註</span><span class="sxs-lookup"><span data-stu-id="4cbaf-119">Remarks</span></span>

<span data-ttu-id="4cbaf-120">**IByteBuffer：： Stat** 方法會抓取 **STATSTRUCT** 結構的指標，其中包含這個開啟資料流程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4cbaf-120">The **IByteBuffer::Stat** method retrieves a pointer to the **STATSTRUCT** structure that contains information about this open stream.</span></span>

## <a name="examples"></a><span data-ttu-id="4cbaf-121">範例</span><span class="sxs-lookup"><span data-stu-id="4cbaf-121">Examples</span></span>

<span data-ttu-id="4cbaf-122">下列範例會示範如何從資料流程中取出統計資訊。</span><span class="sxs-lookup"><span data-stu-id="4cbaf-122">The following example shows retrieving statistical information from the stream.</span></span>


```C++
STATSTRUCT  statstr;
HRESULT     hr;

// Retrieve the statistical information.
hr = pIByteBuff->Stat(&statstr,
                      STATFLAG_DEFAULT);
if (FAILED(hr))
  printf("Failed IByteBuffer::Stat\n");
else
  // Use statstr as needed.
```



## <a name="requirements"></a><span data-ttu-id="4cbaf-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="4cbaf-123">Requirements</span></span>



| <span data-ttu-id="4cbaf-124">需求</span><span class="sxs-lookup"><span data-stu-id="4cbaf-124">Requirement</span></span> | <span data-ttu-id="4cbaf-125">值</span><span class="sxs-lookup"><span data-stu-id="4cbaf-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cbaf-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4cbaf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4cbaf-127">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4cbaf-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4cbaf-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4cbaf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4cbaf-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4cbaf-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4cbaf-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="4cbaf-130">End of client support</span></span><br/>    | <span data-ttu-id="4cbaf-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4cbaf-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4cbaf-132">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="4cbaf-132">End of server support</span></span><br/>    | <span data-ttu-id="4cbaf-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4cbaf-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4cbaf-134">標頭</span><span class="sxs-lookup"><span data-stu-id="4cbaf-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cbaf-135"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="4cbaf-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4cbaf-136">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="4cbaf-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="4cbaf-137"><dt>Scardssp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4cbaf-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4cbaf-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4cbaf-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cbaf-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cbaf-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4cbaf-140">IID</span><span class="sxs-lookup"><span data-stu-id="4cbaf-140">IID</span></span><br/>                      | <span data-ttu-id="4cbaf-141">IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="4cbaf-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

