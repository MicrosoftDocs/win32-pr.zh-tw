---
description: 取得 TCP v6 驅動程式物件的參考。
ms.assetid: 9f57ea0b-0ab4-4ef9-9bf1-1f41f72dfbe9
title: ReferenceTcpDriverV6 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriverV6
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: d0a3f56ea59eb753dc7a49d6f6b1d0c48be8abca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996047"
---
# <a name="referencetcpdriverv6-function"></a><span data-ttu-id="275d1-103">ReferenceTcpDriverV6 函式</span><span class="sxs-lookup"><span data-stu-id="275d1-103">ReferenceTcpDriverV6 function</span></span>

<span data-ttu-id="275d1-104">取得 TCP v6 驅動程式物件的參考。</span><span class="sxs-lookup"><span data-stu-id="275d1-104">Obtains a reference to a TCP v6 driver object.</span></span>

## <a name="syntax"></a><span data-ttu-id="275d1-105">語法</span><span class="sxs-lookup"><span data-stu-id="275d1-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ReferenceTcpDriverV6(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a><span data-ttu-id="275d1-106">參數</span><span class="sxs-lookup"><span data-stu-id="275d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="275d1-107">*ppDriverObject* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="275d1-107">*ppDriverObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="275d1-108">**驅動程式 \_ 物件** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="275d1-108">A pointer to a **DRIVER\_OBJECT** structure.</span></span> <span data-ttu-id="275d1-109">如需詳細資訊，請參閱 WDK 的檔。</span><span class="sxs-lookup"><span data-stu-id="275d1-109">For more information, see the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="275d1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="275d1-110">Return value</span></span>

<span data-ttu-id="275d1-111">如果函式成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="275d1-111">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="275d1-112">如果失敗，則會傳回適當的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="275d1-112">If it fails, it will return the appropriate status code.</span></span>

## <a name="remarks"></a><span data-ttu-id="275d1-113">備註</span><span class="sxs-lookup"><span data-stu-id="275d1-113">Remarks</span></span>

<span data-ttu-id="275d1-114">您只能從核心模式呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="275d1-114">This function can be called only from kernel mode.</span></span> <span data-ttu-id="275d1-115">呼叫端必須在物件完成時呼叫 **ObDereferenceObject** 函式，以遞減參考計數。</span><span class="sxs-lookup"><span data-stu-id="275d1-115">The caller must decrement the reference count by calling the **ObDereferenceObject** function when it has finished with the object.</span></span>

<span data-ttu-id="275d1-116">這個函式會在可供下載的 Drvref 中執行。</span><span class="sxs-lookup"><span data-stu-id="275d1-116">This function is implemented in Drvref.lib, which is available for download.</span></span> <span data-ttu-id="275d1-117">請參閱 [Windows 網路驅動程式參考 API 程式庫](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0)。</span><span class="sxs-lookup"><span data-stu-id="275d1-117">See [Windows Network Driver Reference API Library](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span></span>

## <a name="requirements"></a><span data-ttu-id="275d1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="275d1-118">Requirements</span></span>



| <span data-ttu-id="275d1-119">需求</span><span class="sxs-lookup"><span data-stu-id="275d1-119">Requirement</span></span> | <span data-ttu-id="275d1-120">值</span><span class="sxs-lookup"><span data-stu-id="275d1-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="275d1-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="275d1-121">Library</span></span><br/> | <dl> <span data-ttu-id="275d1-122"><dt>Drvref .lib</dt></span><span class="sxs-lookup"><span data-stu-id="275d1-122"><dt>Drvref.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="275d1-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="275d1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="275d1-124">**ReferenceTcpDriver**</span><span class="sxs-lookup"><span data-stu-id="275d1-124">**ReferenceTcpDriver**</span></span>](referencetcpdriver.md)
</dt> </dl>

 

 




