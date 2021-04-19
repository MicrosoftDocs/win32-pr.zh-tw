---
description: 從系統亂數產生器取出指定的隨機位元組數目。
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: SystemPrng 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemPrng
api_type:
- DllExport
api_location:
- Ksecdd.sys
- Cng.sys
ms.openlocfilehash: d847d34ffd11e158170f55599de0ceb3acf3c697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966701"
---
# <a name="systemprng-function"></a><span data-ttu-id="b505b-103">SystemPrng 函式</span><span class="sxs-lookup"><span data-stu-id="b505b-103">SystemPrng function</span></span>

<span data-ttu-id="b505b-104">\[**SystemPrng** 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b505b-104">\[**SystemPrng** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b505b-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="b505b-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b505b-106">相反地，請使用 [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom)。\]</span><span class="sxs-lookup"><span data-stu-id="b505b-106">Instead, use [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]</span></span>

<span data-ttu-id="b505b-107">**SystemPrng** 函式會從系統亂數產生器取出指定的隨機位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b505b-107">The **SystemPrng** function retrieves a specified number of random bytes from the system random number generator.</span></span>

> [!Note]  
> <span data-ttu-id="b505b-108">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="b505b-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="b505b-109">若要呼叫此函數，您必須建立使用者定義的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="b505b-109">To call this function, you must create a user-defined header file.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b505b-110">語法</span><span class="sxs-lookup"><span data-stu-id="b505b-110">Syntax</span></span>


```C++
BOOL SystemPrng(
  _Out_ unsigned char pbRandomData,
  _In_  size_t        cbRandomData
);
```



## <a name="parameters"></a><span data-ttu-id="b505b-111">參數</span><span class="sxs-lookup"><span data-stu-id="b505b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b505b-112">*pbRandomData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b505b-112">*pbRandomData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b505b-113">接收已抓取位元組之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="b505b-113">A pointer to a buffer that receives the retrieved bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b505b-114">*cbRandomData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b505b-114">*cbRandomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b505b-115">要擷取的位元組數。</span><span class="sxs-lookup"><span data-stu-id="b505b-115">The number of bytes to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b505b-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b505b-116">Return value</span></span>

<span data-ttu-id="b505b-117">一律傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="b505b-117">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b505b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b505b-118">Requirements</span></span>



| <span data-ttu-id="b505b-119">需求</span><span class="sxs-lookup"><span data-stu-id="b505b-119">Requirement</span></span> | <span data-ttu-id="b505b-120">值</span><span class="sxs-lookup"><span data-stu-id="b505b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b505b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b505b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b505b-122">僅限 Windows Vista （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b505b-122">Windows Vista with SP1 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                        |
| <span data-ttu-id="b505b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b505b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b505b-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b505b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                           |
| <span data-ttu-id="b505b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b505b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b505b-126"><dt>Windows Server 2008 和 Windows Vista （含 SP1）上的Ksecdd.sys;</dt><dt>Windows 7 和 Windows Server 2008 R2 上的Cng.sys</dt></span><span class="sxs-lookup"><span data-stu-id="b505b-126"><dt>Ksecdd.sys on Windows Server 2008 and Windows Vista with SP1; </dt> <dt>Cng.sys on Windows 7 and Windows Server 2008 R2</dt></span></span> </dl> |



 

 




