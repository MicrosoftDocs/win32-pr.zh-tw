---
description: 抓取所指定檔案物件的基本屬性。
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: NtQueryAttributesFile 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryAttributesFile
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a1d6d2ff20539f5ef65c0886ba51a0dbabafb44d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977462"
---
# <a name="ntqueryattributesfile-function"></a><span data-ttu-id="68825-103">NtQueryAttributesFile 函式</span><span class="sxs-lookup"><span data-stu-id="68825-103">NtQueryAttributesFile function</span></span>

<span data-ttu-id="68825-104">\[您可以在不另行通知的情況下，從 Windows 變更或移除此功能。\]</span><span class="sxs-lookup"><span data-stu-id="68825-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="68825-105">抓取所指定檔案物件的基本屬性。</span><span class="sxs-lookup"><span data-stu-id="68825-105">Retrieves basic attributes for the specified file object.</span></span>

## <a name="syntax"></a><span data-ttu-id="68825-106">語法</span><span class="sxs-lookup"><span data-stu-id="68825-106">Syntax</span></span>


```C++
NTSTATUS NtQueryAttributesFile(
  _In_  POBJECT_ATTRIBUTES      ObjectAttributes,
  _Out_ PFILE_BASIC_INFORMATION FileInformation
);
```



## <a name="parameters"></a><span data-ttu-id="68825-107">參數</span><span class="sxs-lookup"><span data-stu-id="68825-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68825-108">*ObjectAttributes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68825-108">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68825-109">[物件 \_ 屬性](https://msdn.microsoft.com/library/aa491657.aspx)結構的指標，此結構會提供要用於檔案物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="68825-109">A pointer to an [OBJECT\_ATTRIBUTES](https://msdn.microsoft.com/library/aa491657.aspx) structure that supplies the attributes to be used for the file object.</span></span>

</dd> <dt>

<span data-ttu-id="68825-110">*FileInformation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="68825-110">*FileInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68825-111">[File \_ 基本 \_ 資訊](https://msdn.microsoft.com/library/aa491634.aspx)結構的指標，用來接收傳回的檔案屬性資訊。</span><span class="sxs-lookup"><span data-stu-id="68825-111">A pointer to a [FILE\_BASIC\_INFORMATION](https://msdn.microsoft.com/library/aa491634.aspx) structure to receive the returned file attribute information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68825-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="68825-112">Return value</span></span>

<span data-ttu-id="68825-113">傳回 NTSTATUS 或錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="68825-113">Returns an NTSTATUS or error code.</span></span>

<span data-ttu-id="68825-114">在 WDK 中可用的 Ntstatus 標頭檔中，會列出 NTSTATUS 錯誤碼的表單和重要性，並會在 WDK 檔中說明。</span><span class="sxs-lookup"><span data-stu-id="68825-114">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="68825-115">備註</span><span class="sxs-lookup"><span data-stu-id="68825-115">Remarks</span></span>

<span data-ttu-id="68825-116">此函數沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="68825-116">This function has no associated header file.</span></span> <span data-ttu-id="68825-117">相關聯的匯入程式庫（Ntdll.dll）可在 WDK 中使用。</span><span class="sxs-lookup"><span data-stu-id="68825-117">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="68825-118">您也可以使用 [**LoadLibrary**](-loadlibrary.md) 和 [**GetProcAddress**](-getprocaddress-.md) 函數，動態連結至 Ntdll.dll。</span><span class="sxs-lookup"><span data-stu-id="68825-118">You can also use the [**LoadLibrary**](-loadlibrary.md) and [**GetProcAddress**](-getprocaddress-.md) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="68825-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="68825-119">Requirements</span></span>



| <span data-ttu-id="68825-120">需求</span><span class="sxs-lookup"><span data-stu-id="68825-120">Requirement</span></span> | <span data-ttu-id="68825-121">值</span><span class="sxs-lookup"><span data-stu-id="68825-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="68825-122">DLL</span><span class="sxs-lookup"><span data-stu-id="68825-122">DLL</span></span><br/> | <dl> <span data-ttu-id="68825-123"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68825-123"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 




