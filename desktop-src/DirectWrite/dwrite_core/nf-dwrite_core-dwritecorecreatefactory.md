---
UID: NE:dwrite_core.DWriteCoreCreateFactory
title: 'DWriteCoreCreateFactory (dwrite_core .h) '
description: 建立用於後續建立個別 DWriteCore 物件的 factory 物件。
tech.root: DirectWrite
ms.date: 04/21/2021
ms.topic: reference
req.header: dwrite_core.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWriteCoreCreateFactory
- dwrite_core/DWriteCoreCreateFactory
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_core.h
api_name:
- DWriteCoreCreateFactory
ms.openlocfilehash: 6606ad884fd65195e9922d348cc4fe565b95f2ee
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107882133"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a><span data-ttu-id="5fc46-103">DWriteCoreCreateFactory 函數 (dwrite_core .h) </span><span class="sxs-lookup"><span data-stu-id="5fc46-103">DWriteCoreCreateFactory function (dwrite_core.h)</span></span>

<span data-ttu-id="5fc46-104">建立用於後續建立個別 DWriteCore 物件的 factory 物件。</span><span class="sxs-lookup"><span data-stu-id="5fc46-104">Creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5fc46-105">此 API 可作為 [DirectWrite](../direct-write-portal.md)DWriteCore 執行的一部分。</span><span class="sxs-lookup"><span data-stu-id="5fc46-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="5fc46-106">DWriteCore 是 DirectWrite 的其中一種形式，可在低至 Windows 8 的 Windows 版本上執行，並讓您自由地跨平台使用。</span><span class="sxs-lookup"><span data-stu-id="5fc46-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="5fc46-107">如需詳細資訊和程式碼範例，請參閱 [DWriteCore 總覽](/windows/win32/DirectWrite/dwrite/dwritecore-overview)。</span><span class="sxs-lookup"><span data-stu-id="5fc46-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="5fc46-108">語法</span><span class="sxs-lookup"><span data-stu-id="5fc46-108">Syntax</span></span>
```cpp
HRESULT DWRITE_EXPORT DWriteCoreCreateFactory(
    _In_ DWRITE_FACTORY_TYPE factoryType,
    _In_ REFIID iid,
    _COM_Outptr_ IUnknown** factory
);
```

## <a name="parameters"></a><span data-ttu-id="5fc46-109">參數</span><span class="sxs-lookup"><span data-stu-id="5fc46-109">Parameters</span></span>

`factoryType`

<span data-ttu-id="5fc46-110">類型： <b> <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span><span class="sxs-lookup"><span data-stu-id="5fc46-110">Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span></span>

<span data-ttu-id="5fc46-111">值，這個值會指定是否要共用、隔離或限制 factory 物件。</span><span class="sxs-lookup"><span data-stu-id="5fc46-111">A value that specifies whether the factory object will be shared, isolated, or restricted.</span></span>

`iid`

<span data-ttu-id="5fc46-112">類型： <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="5fc46-112">Type: <b>REFIID</b></span></span>

<span data-ttu-id="5fc46-113">識別 DirectWrite factory 介面的 GUID 值，例如 __uuidof (<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>) 。</span><span class="sxs-lookup"><span data-stu-id="5fc46-113">A GUID value that identifies the DirectWrite factory interface, such as __uuidof(<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).</span></span>

`factory`

<span data-ttu-id="5fc46-114">類型： <b>IUnknown \* \*</b></span><span class="sxs-lookup"><span data-stu-id="5fc46-114">Type: <b>IUnknown\*\*</b></span></span>

<span data-ttu-id="5fc46-115">新建立之 DirectWrite factory 物件的指標位址。</span><span class="sxs-lookup"><span data-stu-id="5fc46-115">An address of a pointer to the newly created DirectWrite factory object.</span></span>

## <a name="return-value"></a><span data-ttu-id="5fc46-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5fc46-116">Return value</span></span>

<span data-ttu-id="5fc46-117">類型： <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="5fc46-117">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="5fc46-118">如果這個方法成功，它會傳回 <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>。</span><span class="sxs-lookup"><span data-stu-id="5fc46-118">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="5fc46-119">否則，它會傳回 <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5fc46-119">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="5fc46-120">範例</span><span class="sxs-lookup"><span data-stu-id="5fc46-120">Examples</span></span>

<span data-ttu-id="5fc46-121">請參閱 [DWriteCore 總覽](/windows/win32/DirectWrite/dwrite/dwritecore-overview) 主題和 [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) 範例應用程式。</span><span class="sxs-lookup"><span data-stu-id="5fc46-121">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fc46-122">備註</span><span class="sxs-lookup"><span data-stu-id="5fc46-122">Remarks</span></span>

<span data-ttu-id="5fc46-123">其功能與系統版本 DirectWrite 所匯出的 [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) 函式相同。</span><span class="sxs-lookup"><span data-stu-id="5fc46-123">This is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="5fc46-124">DWriteCore 函式有不同的名稱，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="5fc46-124">The DWriteCore function has a different name to avoid ambiguity.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fc46-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="5fc46-125">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5fc46-126">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="5fc46-126">**Minimum supported client**</span></span> | <span data-ttu-id="5fc46-127">Windows 10，專案留尼旺島 [Win32 apps]</span><span class="sxs-lookup"><span data-stu-id="5fc46-127">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="5fc46-128">**標頭**</span><span class="sxs-lookup"><span data-stu-id="5fc46-128">**Header**</span></span> | <span data-ttu-id="5fc46-129">dwrite (包含 dwrite_core .h) </span><span class="sxs-lookup"><span data-stu-id="5fc46-129">dwrite.h (include dwrite_core.h)</span></span> |
