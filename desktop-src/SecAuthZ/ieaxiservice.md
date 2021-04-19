---
description: 當目前的使用者沒有安裝物件的許可權時，初始化系統服務物件以安裝 ActiveX 物件。
ms.assetid: 42f7cf83-789b-42ea-bb1a-4b79137188ea
title: IeAxiService 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService
api_type:
- COM
api_location: ''
ms.openlocfilehash: 34c4743327b2539616dee6b09c34d9f479aa3303
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001404"
---
# <a name="ieaxiservice-interface"></a><span data-ttu-id="5ca15-103">IeAxiService 介面</span><span class="sxs-lookup"><span data-stu-id="5ca15-103">IeAxiService interface</span></span>

<span data-ttu-id="5ca15-104">當目前的使用者沒有安裝物件的許可權時， **IAxiService** 介面會初始化系統服務物件以安裝 ActiveX 物件。</span><span class="sxs-lookup"><span data-stu-id="5ca15-104">The **IAxiService** interface initializes a system service object to install an ActiveX object when the current user does not have permission to install the object.</span></span>

<span data-ttu-id="5ca15-105">[**CIeAxiInstallerService**](cieaxiinstallerservice.md)類別會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="5ca15-105">The [**CIeAxiInstallerService**](cieaxiinstallerservice.md) class implements this interface.</span></span>

<span data-ttu-id="5ca15-106">未在公用標頭中宣告此介面。</span><span class="sxs-lookup"><span data-stu-id="5ca15-106">This interface is not declared in a public header.</span></span> <span data-ttu-id="5ca15-107">應用程式必須自行定義。</span><span class="sxs-lookup"><span data-stu-id="5ca15-107">Applications must define it themselves.</span></span> <span data-ttu-id="5ca15-108">下列介面定義語言 (IDL) 片段描述這個介面，包括其 IID。</span><span class="sxs-lookup"><span data-stu-id="5ca15-108">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(E9E92380-9ECD-4982-A0EB-6815A56CCF27),
    pointer_default(unique)
]

interface IeAxiService : IUnknown{

    
    HRESULT Initialize(
            [in]        HWND            hwndParent,
            [in]        DWORD           dwClientPID,
            [in]        BSTR            bstrDesktop,
            [in]        BSTR            bstrClsID,              
            [in]        BSTR            bstrURL,                
            [out]       BSTR *          pbstrNonce,            
            [out]       IUnknown**      ppISyncBrokerInterface  
            );  
 
    HRESULT Cleanup();
};
```

## <a name="members"></a><span data-ttu-id="5ca15-109">成員</span><span class="sxs-lookup"><span data-stu-id="5ca15-109">Members</span></span>

<span data-ttu-id="5ca15-110">**IeAxiService** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="5ca15-110">The **IeAxiService** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5ca15-111">**IeAxiService** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5ca15-111">**IeAxiService** also has these types of members:</span></span>

-   [<span data-ttu-id="5ca15-112">方法</span><span class="sxs-lookup"><span data-stu-id="5ca15-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5ca15-113">方法</span><span class="sxs-lookup"><span data-stu-id="5ca15-113">Methods</span></span>

<span data-ttu-id="5ca15-114">**IeAxiService** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="5ca15-114">The **IeAxiService** interface has these methods.</span></span>



| <span data-ttu-id="5ca15-115">方法</span><span class="sxs-lookup"><span data-stu-id="5ca15-115">Method</span></span>                                        | <span data-ttu-id="5ca15-116">描述</span><span class="sxs-lookup"><span data-stu-id="5ca15-116">Description</span></span>                                                        |
|:----------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="5ca15-117">**清除**</span><span class="sxs-lookup"><span data-stu-id="5ca15-117">**Cleanup**</span></span>](ieaxiservice-cleanup.md)       | <span data-ttu-id="5ca15-118">釋放 **IeAxiService** 介面使用的資源。</span><span class="sxs-lookup"><span data-stu-id="5ca15-118">Frees resources used by the **IeAxiService** interface.</span></span><br/> |
| [<span data-ttu-id="5ca15-119">**初始化**</span><span class="sxs-lookup"><span data-stu-id="5ca15-119">**Initialize**</span></span>](ieaxiservice-initialize.md) | <span data-ttu-id="5ca15-120">檢查和下載 ActiveX 物件。</span><span class="sxs-lookup"><span data-stu-id="5ca15-120">Checks and downloads an ActiveX object.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="5ca15-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ca15-121">Requirements</span></span>



| <span data-ttu-id="5ca15-122">需求</span><span class="sxs-lookup"><span data-stu-id="5ca15-122">Requirement</span></span> | <span data-ttu-id="5ca15-123">值</span><span class="sxs-lookup"><span data-stu-id="5ca15-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca15-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ca15-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5ca15-125">Windows Vista Business、Windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ca15-125">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5ca15-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ca15-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5ca15-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="5ca15-127">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="5ca15-128">IID</span><span class="sxs-lookup"><span data-stu-id="5ca15-128">IID</span></span><br/>                      | <span data-ttu-id="5ca15-129">IID \_ IeAxiService 定義為 E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="5ca15-129">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



 

