---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: 'DWRITE_FACTORY_TYPE (DWRITE) '
description: 指定 DirectWrite factory 物件的類型。
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite.h
req.include-header: dwrite_core.h
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
- DWRITE_FACTORY_TYPE
- dwrite/DWRITE_FACTORY_TYPE
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite.h
api_name:
- DWRITE_FACTORY_TYPE
ms.openlocfilehash: 87b0d1c2edcb836afd06d732f242b62441b9bd01
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881807"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a><span data-ttu-id="3c975-103">DWRITE_FACTORY_TYPE 列舉 (DWRITE .h) </span><span class="sxs-lookup"><span data-stu-id="3c975-103">DWRITE_FACTORY_TYPE enumeration (dwrite.h)</span></span>

<span data-ttu-id="3c975-104">指定 DirectWrite factory 物件的類型。</span><span class="sxs-lookup"><span data-stu-id="3c975-104">Specifies the type of DirectWrite factory object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3c975-105">此 API 可作為 [DirectWrite](../direct-write-portal.md)DWriteCore 執行的一部分。</span><span class="sxs-lookup"><span data-stu-id="3c975-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="3c975-106">DWriteCore 是 DirectWrite 的其中一種形式，可在低至 Windows 8 的 Windows 版本上執行，並讓您自由地跨平台使用。</span><span class="sxs-lookup"><span data-stu-id="3c975-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="3c975-107">如需詳細資訊和程式碼範例，請參閱 [DWriteCore 總覽](/windows/win32/DirectWrite/dwrite/dwritecore-overview)。</span><span class="sxs-lookup"><span data-stu-id="3c975-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="3c975-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c975-108">Syntax</span></span>
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_ISOLATED2
} ;
```

## <a name="constants"></a><span data-ttu-id="3c975-109">常數</span><span class="sxs-lookup"><span data-stu-id="3c975-109">Constants</span></span>

| <span data-ttu-id="3c975-110">Name</span><span class="sxs-lookup"><span data-stu-id="3c975-110">Name</span></span> | <span data-ttu-id="3c975-111">描述</span><span class="sxs-lookup"><span data-stu-id="3c975-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="3c975-112">DWRITE_FACTORY_TYPE_SHARED</span><span class="sxs-lookup"><span data-stu-id="3c975-112">DWRITE_FACTORY_TYPE_SHARED</span></span> | <span data-ttu-id="3c975-113">指出 DirectWrite factory 是共用的處理站，它允許在多個同進程元件之間重複使用快取的字型資料。</span><span class="sxs-lookup"><span data-stu-id="3c975-113">Indicates that the DirectWrite factory is a shared factory and that it allows for the reuse of cached font data across multiple in-process components.</span></span> <span data-ttu-id="3c975-114">這類工廠也會利用跨進程的字型快取元件，以獲得更好的效能。</span><span class="sxs-lookup"><span data-stu-id="3c975-114">Such factories also take advantage of cross process font caching components for better performance.</span></span> |
| <span data-ttu-id="3c975-115">DWRITE_FACTORY_TYPE_ISOLATED</span><span class="sxs-lookup"><span data-stu-id="3c975-115">DWRITE_FACTORY_TYPE_ISOLATED</span></span> | <span data-ttu-id="3c975-116">表示 DirectWrite factory 物件已隔離。</span><span class="sxs-lookup"><span data-stu-id="3c975-116">Indicates that the DirectWrite factory object is isolated.</span></span> <span data-ttu-id="3c975-117">從隔離處理站建立的物件不會與其他元件的內部 DirectWrite 狀態互動。</span><span class="sxs-lookup"><span data-stu-id="3c975-117">Objects created from the isolated factory do not interact with internal DirectWrite state from other components.</span></span> |
| <span data-ttu-id="3c975-118">DWRITE_FACTORY_TYPE_ISOLATED2</span><span class="sxs-lookup"><span data-stu-id="3c975-118">DWRITE_FACTORY_TYPE_ISOLATED2</span></span> | <span data-ttu-id="3c975-119">表示已限制 DirectWrite factory 物件。</span><span class="sxs-lookup"><span data-stu-id="3c975-119">Indicates that the DirectWrite factory object is restricted.</span></span> <span data-ttu-id="3c975-120">從受限制的處理站建立的物件不會使用或修改其他處理站所使用的內部狀態或快取資料。</span><span class="sxs-lookup"><span data-stu-id="3c975-120">Objects created from a restricted factory don't use nor modify internal state or cached data used by other factories.</span></span> <span data-ttu-id="3c975-121">此外，系統字型集合只包含已知字型。</span><span class="sxs-lookup"><span data-stu-id="3c975-121">In addition, the system font collection contains only well-known fonts.</span></span>|

## <a name="examples"></a><span data-ttu-id="3c975-122">範例</span><span class="sxs-lookup"><span data-stu-id="3c975-122">Examples</span></span>

<span data-ttu-id="3c975-123">請參閱 [DWriteCore 總覽](/windows/win32/DirectWrite/dwrite/dwritecore-overview) 主題和 [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) 範例應用程式。</span><span class="sxs-lookup"><span data-stu-id="3c975-123">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c975-124">備註</span><span class="sxs-lookup"><span data-stu-id="3c975-124">Remarks</span></span>

<span data-ttu-id="3c975-125">DirectWrite factory 物件包含其內部狀態的相關資訊，例如字型載入器註冊和快取的字型資料。</span><span class="sxs-lookup"><span data-stu-id="3c975-125">A DirectWrite factory object contains information about its internal state, such as font loader registration and cached font data.</span></span> <span data-ttu-id="3c975-126">在大部分情況下，您應該使用共用處理站物件，因為它允許使用 DirectWrite 的多個元件共用內部 DirectWrite 狀態資訊，進而減少記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="3c975-126">In most cases you should use the shared factory object, because it allows multiple components that use DirectWrite to share internal DirectWrite state information, thereby reducing memory usage.</span></span> <span data-ttu-id="3c975-127">不過，在某些情況下，您可能會想要將元件的影響減少到進程的其餘部分，例如來自不受信任來源的外掛程式，方法是將它與其余的進程元件進行沙箱化並隔離。</span><span class="sxs-lookup"><span data-stu-id="3c975-127">However, there are cases when it is desirable to reduce the impact of a component on the rest of the process, such as a plug-in from an untrusted source,  by sandboxing and isolating it from the rest of the process components.</span></span> <span data-ttu-id="3c975-128">在這種情況下，您應該使用沙箱元件的隔離處理站。</span><span class="sxs-lookup"><span data-stu-id="3c975-128">In such cases, you should use an isolated factory for the sandboxed component.</span></span>

<span data-ttu-id="3c975-129">受限制的處理站比隔離處理站更受鎖定。</span><span class="sxs-lookup"><span data-stu-id="3c975-129">A restricted factory is more locked down than an isolated factory.</span></span> <span data-ttu-id="3c975-130">它不會以任何方式與跨進程或持續性的字型快取互動。</span><span class="sxs-lookup"><span data-stu-id="3c975-130">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="3c975-131">此外，從這個 factory 傳回的系統字型集合只包含已知字型。</span><span class="sxs-lookup"><span data-stu-id="3c975-131">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="3c975-132">如果您將 **DWRITE_FACTORY_TYPE_ISOLATED2** 傳遞給早于 DWriteCore 的 DWRITE 版本，則 [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) 會傳回 **E_INVALIDARG**。</span><span class="sxs-lookup"><span data-stu-id="3c975-132">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to a version of DWrite that's older than DWriteCore, then [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) returns **E_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c975-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c975-133">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3c975-134">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="3c975-134">**Minimum supported client**</span></span> | <span data-ttu-id="3c975-135">Windows 10，專案留尼旺島 [Win32 apps]</span><span class="sxs-lookup"><span data-stu-id="3c975-135">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="3c975-136">**標頭**</span><span class="sxs-lookup"><span data-stu-id="3c975-136">**Header**</span></span> | <span data-ttu-id="3c975-137">dwrite (包含 dwrite_core .h) </span><span class="sxs-lookup"><span data-stu-id="3c975-137">dwrite.h (include dwrite_core.h)</span></span> |
