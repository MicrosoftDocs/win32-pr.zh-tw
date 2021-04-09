---
Description: 從 Apphelp 詳細資料資料庫中取出資料。
ms.assetid: f3731561-bf3f-4139-9890-bd4ce73d83fa
title: SdbReadApphelpDetailsData 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadApphelpDetailsData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a0a352e3fe33115133b827b5ad03d99a14101b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934310"
---
# <a name="sdbreadapphelpdetailsdata-function"></a><span data-ttu-id="33676-103">SdbReadApphelpDetailsData 函式</span><span class="sxs-lookup"><span data-stu-id="33676-103">SdbReadApphelpDetailsData function</span></span>

<span data-ttu-id="33676-104">從 Apphelp 詳細資料資料庫中取出資料。</span><span class="sxs-lookup"><span data-stu-id="33676-104">Retrieves data from the Apphelp details database.</span></span>

## <a name="syntax"></a><span data-ttu-id="33676-105">語法</span><span class="sxs-lookup"><span data-stu-id="33676-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadApphelpDetailsData(
  _In_  PDB           pdb,
  _Out_ PAPPHELP_DATA pData
);
```



## <a name="parameters"></a><span data-ttu-id="33676-106">參數</span><span class="sxs-lookup"><span data-stu-id="33676-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33676-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33676-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33676-108">Apphelp details 資料庫 Apphelp 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="33676-108">A handle to the Apphelp details database, Apphelp.sdb.</span></span>

</dd> <dt>

<span data-ttu-id="33676-109">*.pdata* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="33676-109">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33676-110">[**APPHELP \_ 資料**](apphelp-data.md)結構。</span><span class="sxs-lookup"><span data-stu-id="33676-110">An [**APPHELP\_DATA**](apphelp-data.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33676-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="33676-111">Return value</span></span>

<span data-ttu-id="33676-112">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="33676-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="33676-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="33676-113">Requirements</span></span>



| <span data-ttu-id="33676-114">需求</span><span class="sxs-lookup"><span data-stu-id="33676-114">Requirement</span></span> | <span data-ttu-id="33676-115">值</span><span class="sxs-lookup"><span data-stu-id="33676-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33676-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33676-116">Minimum supported client</span></span><br/> | <span data-ttu-id="33676-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33676-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="33676-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33676-118">Minimum supported server</span></span><br/> | <span data-ttu-id="33676-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33676-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="33676-120">DLL</span><span class="sxs-lookup"><span data-stu-id="33676-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33676-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33676-121"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




