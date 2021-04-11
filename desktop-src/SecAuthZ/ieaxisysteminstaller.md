---
description: 安裝 ActiveX 物件。
ms.assetid: 0eb725a9-ceb8-40e5-808d-ac2b286a48b6
title: IeAxiSystemInstaller 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 391088a70aa845cd685511f10e4eb6e809dc7fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027351"
---
# <a name="ieaxisysteminstaller-interface"></a><span data-ttu-id="61790-103">IeAxiSystemInstaller 介面</span><span class="sxs-lookup"><span data-stu-id="61790-103">IeAxiSystemInstaller interface</span></span>

<span data-ttu-id="61790-104">**IeAxiSystemInstaller** 介面會安裝 ActiveX 物件。</span><span class="sxs-lookup"><span data-stu-id="61790-104">The **IeAxiSystemInstaller** interface installs an ActiveX object.</span></span>

<span data-ttu-id="61790-105">未在公用標頭中宣告此介面。</span><span class="sxs-lookup"><span data-stu-id="61790-105">This interface is not declared in a public header.</span></span> <span data-ttu-id="61790-106">應用程式必須自行定義。</span><span class="sxs-lookup"><span data-stu-id="61790-106">Applications must define it themselves.</span></span> <span data-ttu-id="61790-107">下列介面定義語言 (IDL) 片段描述這個介面，包括其 IID。</span><span class="sxs-lookup"><span data-stu-id="61790-107">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(a50ea6f8-4764-4299-b309-022b2a8b4d8d),
    
]
interface IeAxiSystemInstaller : IUnknown
{
    
    HRESULT InitializeSystemInstaller(  [in] BSTR bstrUrl,
                                  [in] DWORD dwClientPID,
                                  [in] IUnknown* pCallback,
                                  [out] BSTR * pbstrNonce);
}

```

## <a name="members"></a><span data-ttu-id="61790-108">成員</span><span class="sxs-lookup"><span data-stu-id="61790-108">Members</span></span>

<span data-ttu-id="61790-109">**IeAxiSystemInstaller** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="61790-109">The **IeAxiSystemInstaller** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="61790-110">**IeAxiSystemInstaller** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="61790-110">**IeAxiSystemInstaller** also has these types of members:</span></span>

-   [<span data-ttu-id="61790-111">方法</span><span class="sxs-lookup"><span data-stu-id="61790-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="61790-112">方法</span><span class="sxs-lookup"><span data-stu-id="61790-112">Methods</span></span>

<span data-ttu-id="61790-113">**IeAxiSystemInstaller** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="61790-113">The **IeAxiSystemInstaller** interface has these methods.</span></span>



| <span data-ttu-id="61790-114">方法</span><span class="sxs-lookup"><span data-stu-id="61790-114">Method</span></span>                                                                              | <span data-ttu-id="61790-115">描述</span><span class="sxs-lookup"><span data-stu-id="61790-115">Description</span></span>                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="61790-116">**InitializeSystemInstaller**</span><span class="sxs-lookup"><span data-stu-id="61790-116">**InitializeSystemInstaller**</span></span>](ieaxisysteminstaller-initializesysteminstaller.md) | <span data-ttu-id="61790-117">安裝指定的 ActiveX 物件。</span><span class="sxs-lookup"><span data-stu-id="61790-117">Installs the specified ActiveX object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="61790-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="61790-118">Requirements</span></span>



| <span data-ttu-id="61790-119">需求</span><span class="sxs-lookup"><span data-stu-id="61790-119">Requirement</span></span> | <span data-ttu-id="61790-120">值</span><span class="sxs-lookup"><span data-stu-id="61790-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61790-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61790-121">Minimum supported client</span></span><br/> | <span data-ttu-id="61790-122">Windows Vista Business、Windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61790-122">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="61790-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61790-123">Minimum supported server</span></span><br/> | <span data-ttu-id="61790-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="61790-124">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="61790-125">IID</span><span class="sxs-lookup"><span data-stu-id="61790-125">IID</span></span><br/>                      | <span data-ttu-id="61790-126">IID \_ IeAxiSystemInstaller 定義為 a50ea6f8-4764-4299-b309-022b2a8b4d8d</span><span class="sxs-lookup"><span data-stu-id="61790-126">IID\_IeAxiSystemInstaller is defined as a50ea6f8-4764-4299-b309-022b2a8b4d8d</span></span><br/>                   |



 

