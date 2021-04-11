---
description: 針對指定的 TAGREF，抓取 TAGID 和填充碼資料庫的控制碼。
ms.assetid: 869c6af5-4c10-4358-9d6a-1a354be6f4e9
title: SdbTagRefToTagID 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagRefToTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: faff00adc25a741342e586adea2f645a62eca36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110425"
---
# <a name="sdbtagreftotagid-function"></a><span data-ttu-id="a6693-103">SdbTagRefToTagID 函式</span><span class="sxs-lookup"><span data-stu-id="a6693-103">SdbTagRefToTagID function</span></span>

<span data-ttu-id="a6693-104">針對指定的 [**TAGREF**](tagref.md)，抓取 **TAGID** 和填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a6693-104">Retrieves the **TAGID** and a handle to the shim database for the specified [**TAGREF**](tagref.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a6693-105">語法</span><span class="sxs-lookup"><span data-stu-id="a6693-105">Syntax</span></span>


```C++
BOOL WINAPI SdbTagRefToTagID(
  _In_  HSDB   hSDB,
  _In_  TAGREF trWhich,
  _Out_ PDB    *ppdb,
  _Out_ TAGID  *ptiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="a6693-106">參數</span><span class="sxs-lookup"><span data-stu-id="a6693-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6693-107">*hSDB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6693-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6693-108">[**SdbInitDatabase**](sdbinitdatabase.md)函式所傳回之填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a6693-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a6693-109">*trWhich* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6693-109">*trWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6693-110">[**TAGREF**](tagref.md)。</span><span class="sxs-lookup"><span data-stu-id="a6693-110">The [**TAGREF**](tagref.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6693-111">*ppdb* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a6693-111">*ppdb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6693-112">填充碼資料庫產生的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a6693-112">The resulting handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="a6693-113">*ptiWhich* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a6693-113">*ptiWhich* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6693-114">產生的 **TAGID**。</span><span class="sxs-lookup"><span data-stu-id="a6693-114">The resulting **TAGID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6693-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a6693-115">Return value</span></span>

<span data-ttu-id="a6693-116">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a6693-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6693-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6693-117">Requirements</span></span>



| <span data-ttu-id="a6693-118">需求</span><span class="sxs-lookup"><span data-stu-id="a6693-118">Requirement</span></span> | <span data-ttu-id="a6693-119">值</span><span class="sxs-lookup"><span data-stu-id="a6693-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6693-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6693-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a6693-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6693-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a6693-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6693-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a6693-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6693-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a6693-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a6693-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6693-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6693-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6693-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6693-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6693-127">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="a6693-127">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> <dt>

[<span data-ttu-id="a6693-128">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="a6693-128">**TAGID**</span></span>](tagid.md)
</dt> <dt>

[<span data-ttu-id="a6693-129">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="a6693-129">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




