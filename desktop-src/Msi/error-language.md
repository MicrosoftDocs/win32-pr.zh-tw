---
description: Error 物件的唯讀語言屬性會傳回目前錯誤的 LANGID。
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
title: '錯誤。 Language 屬性 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Language
- IMsmError.get_Language
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 6c80802c41f076a2b1c0b320b591bc591da8546e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992982"
---
# <a name="errorlanguage-property"></a><span data-ttu-id="abc53-103">錯誤。語言屬性</span><span class="sxs-lookup"><span data-stu-id="abc53-103">Error.Language property</span></span>

<span data-ttu-id="abc53-104">[**Error**](error-object.md)物件的唯讀 **語言** 屬性會傳回目前錯誤的 **LANGID** 。</span><span class="sxs-lookup"><span data-stu-id="abc53-104">The read-only **Language** property of the [**Error**](error-object.md) object returns the **LANGID** of the current error.</span></span>

<span data-ttu-id="abc53-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="abc53-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="abc53-106">語法</span><span class="sxs-lookup"><span data-stu-id="abc53-106">Syntax</span></span>


```JScript
propVal = Error.Language
```



## <a name="property-value"></a><span data-ttu-id="abc53-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="abc53-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="abc53-108">備註</span><span class="sxs-lookup"><span data-stu-id="abc53-108">Remarks</span></span>

<span data-ttu-id="abc53-109">除非錯誤的類型為 msmErrorLanguageUnsupported 或 msmErrorLanguageFailed，否則 **Language** 屬性的值為-1。</span><span class="sxs-lookup"><span data-stu-id="abc53-109">The value of the **Language** property is -1 unless the error is of type msmErrorLanguageUnsupported or msmErrorLanguageFailed.</span></span> <span data-ttu-id="abc53-110">您可以藉由呼叫 [**錯誤**](error-object.md)物件的 [**type**](error-type.md)屬性來判斷錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="abc53-110">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="abc53-111">C++</span><span class="sxs-lookup"><span data-stu-id="abc53-111">C++</span></span>

<span data-ttu-id="abc53-112">請參閱 [**取得 \_ Language Function (Error 物件)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language)。</span><span class="sxs-lookup"><span data-stu-id="abc53-112">See [**get\_Language Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).</span></span>

## <a name="requirements"></a><span data-ttu-id="abc53-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="abc53-113">Requirements</span></span>



| <span data-ttu-id="abc53-114">需求</span><span class="sxs-lookup"><span data-stu-id="abc53-114">Requirement</span></span> | <span data-ttu-id="abc53-115">值</span><span class="sxs-lookup"><span data-stu-id="abc53-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abc53-116">版本</span><span class="sxs-lookup"><span data-stu-id="abc53-116">Version</span></span><br/> | <span data-ttu-id="abc53-117">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="abc53-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="abc53-118">標頭</span><span class="sxs-lookup"><span data-stu-id="abc53-118">Header</span></span><br/>  | <dl> <span data-ttu-id="abc53-119"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="abc53-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="abc53-120">DLL</span><span class="sxs-lookup"><span data-stu-id="abc53-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="abc53-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abc53-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

