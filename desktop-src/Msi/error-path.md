---
description: 在 Windows Installer 1.0 和1.1 版中，Path 屬性一律為空字串。 未來的版本可能會使用這個值，傳回無法建立之檔案或目錄的路徑。
ms.assetid: b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b
title: '錯誤。 Path 屬性 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Path
- IMsmError.get_Path
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5a2e462790d6f929943fe2fe364228cd73d3deb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981341"
---
# <a name="errorpath-property"></a><span data-ttu-id="6f309-104">錯誤。 Path 屬性</span><span class="sxs-lookup"><span data-stu-id="6f309-104">Error.Path property</span></span>

<span data-ttu-id="6f309-105">在 Windows Installer 1.0 和1.1 版中，Path 屬性一律為空字串。</span><span class="sxs-lookup"><span data-stu-id="6f309-105">In Windows Installer versions 1.0 and 1.1 the Path property is always the empty string.</span></span> <span data-ttu-id="6f309-106">未來的版本可能會使用這個值，傳回無法建立之檔案或目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="6f309-106">Future versions may use this value to return the path to the file or directory that could not be created.</span></span>

<span data-ttu-id="6f309-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6f309-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f309-108">語法</span><span class="sxs-lookup"><span data-stu-id="6f309-108">Syntax</span></span>


```JScript
propVal = Error.Path
```



## <a name="property-value"></a><span data-ttu-id="6f309-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="6f309-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="6f309-110">備註</span><span class="sxs-lookup"><span data-stu-id="6f309-110">Remarks</span></span>

<span data-ttu-id="6f309-111">此值只對 msmErrorFileCreate 或 msmErrorDirCreate 類型的錯誤有效。</span><span class="sxs-lookup"><span data-stu-id="6f309-111">This value is only valid for errors of type msmErrorFileCreate or msmErrorDirCreate.</span></span> <span data-ttu-id="6f309-112">您可以藉由呼叫 [**error**](error-object.md)物件的 [**type**](error-type.md)屬性來判斷錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="6f309-112">You can determine the type of error by calling [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="6f309-113">C++</span><span class="sxs-lookup"><span data-stu-id="6f309-113">C++</span></span>

<span data-ttu-id="6f309-114">請參閱 [**get \_ Path**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) 函數。</span><span class="sxs-lookup"><span data-stu-id="6f309-114">See [**get\_Path**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f309-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f309-115">Requirements</span></span>



| <span data-ttu-id="6f309-116">需求</span><span class="sxs-lookup"><span data-stu-id="6f309-116">Requirement</span></span> | <span data-ttu-id="6f309-117">值</span><span class="sxs-lookup"><span data-stu-id="6f309-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f309-118">版本</span><span class="sxs-lookup"><span data-stu-id="6f309-118">Version</span></span><br/> | <span data-ttu-id="6f309-119">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6f309-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="6f309-120">標頭</span><span class="sxs-lookup"><span data-stu-id="6f309-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6f309-121"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="6f309-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f309-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6f309-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="6f309-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f309-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

