---
description: 從 BLOB NPP 區段的 NetworkInfo 類別中抓取 MAC 類型，並將類型資料轉換成 MAC 類型號碼。
ms.assetid: 53aa538c-69ee-4b34-93fb-9e61c6baadea
title: 'GetNPPMacTypeAsNumber 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPMacTypeAsNumber
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9174b1deeb04d8d9665509daeff56d832d447892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510973"
---
# <a name="getnppmactypeasnumber-function"></a><span data-ttu-id="6ba27-103">GetNPPMacTypeAsNumber 函式</span><span class="sxs-lookup"><span data-stu-id="6ba27-103">GetNPPMacTypeAsNumber function</span></span>

<span data-ttu-id="6ba27-104">**GetNPPMacTypeAsNumber** 函式會從 BLOB 的 NPP 區段的 NetworkInfo 類別中抓取 mac 類型，並將類型資料轉換成 MAC 類型號碼。</span><span class="sxs-lookup"><span data-stu-id="6ba27-104">The **GetNPPMacTypeAsNumber** function retrieves the MAC type from the NetworkInfo category of the NPP section of the BLOB and converts the type data into a MAC type number.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ba27-105">語法</span><span class="sxs-lookup"><span data-stu-id="6ba27-105">Syntax</span></span>


```C++
DWORD GetNPPMacTypeAsNumber(
  _In_  HBLOB   hBlob,
  _Out_ LPDWORD lpMacType
);
```



## <a name="parameters"></a><span data-ttu-id="6ba27-106">參數</span><span class="sxs-lookup"><span data-stu-id="6ba27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ba27-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ba27-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba27-108">指定之 BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6ba27-108">A handle to the specified BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="6ba27-109">*lpMacType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6ba27-109">*lpMacType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba27-110">MAC 型別的指標。</span><span class="sxs-lookup"><span data-stu-id="6ba27-110">A pointer to the MAC type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ba27-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ba27-111">Return value</span></span>

<span data-ttu-id="6ba27-112">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="6ba27-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6ba27-113">如果標記無法使用，則傳回值為 MAC \_ 類型 \_ 未知。</span><span class="sxs-lookup"><span data-stu-id="6ba27-113">If the tag is unavailable, the return value is MAC\_TYPE\_UNKNOWN.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ba27-114">備註</span><span class="sxs-lookup"><span data-stu-id="6ba27-114">Remarks</span></span>

<span data-ttu-id="6ba27-115">此函式會將標記 **NPP： NetworkInfo： MacType** 對應至 Npptypes .h 檔案中定義的 **MAC \_ 類型 \_ \*** 。</span><span class="sxs-lookup"><span data-stu-id="6ba27-115">This function maps the tag, **NPP:NetworkInfo:MacType** to the **MAC\_TYPE\_\*** as defined in the Npptypes.h file.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ba27-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ba27-116">Requirements</span></span>



| <span data-ttu-id="6ba27-117">需求</span><span class="sxs-lookup"><span data-stu-id="6ba27-117">Requirement</span></span> | <span data-ttu-id="6ba27-118">值</span><span class="sxs-lookup"><span data-stu-id="6ba27-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba27-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ba27-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6ba27-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ba27-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6ba27-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ba27-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6ba27-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ba27-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6ba27-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6ba27-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ba27-124"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="6ba27-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="6ba27-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="6ba27-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ba27-126"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ba27-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="6ba27-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6ba27-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ba27-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ba27-128"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




