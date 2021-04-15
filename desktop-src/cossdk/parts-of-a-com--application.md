---
description: COM + 應用程式是由一或多個 COM 元件所組成。
ms.assetid: e7ed2844-276e-4726-952d-e4d3be2eb6e8
title: COM + 應用程式的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f75aba454689e25e8706d4a7e3f059d498891f9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468101"
---
# <a name="parts-of-a-com-application"></a><span data-ttu-id="752aa-103">COM + 應用程式的元件</span><span class="sxs-lookup"><span data-stu-id="752aa-103">Parts of a COM+ Application</span></span>

<span data-ttu-id="752aa-104">COM + 應用程式是由一或多個 COM 元件所組成。</span><span class="sxs-lookup"><span data-stu-id="752aa-104">COM+ applications consist of one or more COM components.</span></span>

<span data-ttu-id="752aa-105">COM + 檔中使用下列詞彙：</span><span class="sxs-lookup"><span data-stu-id="752aa-105">The following terms are used throughout the COM+ documentation:</span></span>

<dl> <dt>

<span data-ttu-id="752aa-106"><span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*COM 元件*</span><span class="sxs-lookup"><span data-stu-id="752aa-106"><span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*COM component*</span></span>
</dt> <dd>

<span data-ttu-id="752aa-107">建立 COM 物件 (包含封裝和註冊程式碼) 的二進位單位程式碼。</span><span class="sxs-lookup"><span data-stu-id="752aa-107">A binary unit of code that creates COM objects (includes packaging and registration code).</span></span>

</dd> <dt>

<span data-ttu-id="752aa-108"><span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*COM 物件*</span><span class="sxs-lookup"><span data-stu-id="752aa-108"><span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*COM object*</span></span>
</dt> <dd>

<span data-ttu-id="752aa-109">COM 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="752aa-109">An instance of a COM class.</span></span>

</dd> <dt>

<span data-ttu-id="752aa-110"><span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*COM 類別*</span><span class="sxs-lookup"><span data-stu-id="752aa-110"><span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*COM class*</span></span>
</dt> <dd>

<span data-ttu-id="752aa-111">一或多個介面的已命名、具體實作為。</span><span class="sxs-lookup"><span data-stu-id="752aa-111">A named, concrete implementation of one or more interfaces.</span></span> <span data-ttu-id="752aa-112">COM 類別是以 CLSID 識別 (有時也會) ProgID。</span><span class="sxs-lookup"><span data-stu-id="752aa-112">A COM class is identified by a CLSID (sometimes by a ProgID also).</span></span>

</dd> <dt>

<span data-ttu-id="752aa-113"><span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*COM 介面*</span><span class="sxs-lookup"><span data-stu-id="752aa-113"><span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*COM interface*</span></span>
</dt> <dd>

<span data-ttu-id="752aa-114">由指定合約的 COM 類別所公開的一組相關的方法函數。</span><span class="sxs-lookup"><span data-stu-id="752aa-114">A group of related method functions exposed by a COM class that specify a contract.</span></span> <span data-ttu-id="752aa-115">這包括 name、interface signature、interface 語義和封送處理緩衝區格式。</span><span class="sxs-lookup"><span data-stu-id="752aa-115">This includes the name, interface signature, interface semantics, and marshaling buffer format.</span></span> <span data-ttu-id="752aa-116">介面是由 IID 識別。</span><span class="sxs-lookup"><span data-stu-id="752aa-116">An interface is identified by an IID.</span></span> <span data-ttu-id="752aa-117">介面語法定義于 IDL 和/或類型程式庫中。</span><span class="sxs-lookup"><span data-stu-id="752aa-117">The interface syntax is defined in IDL and/or type libraries.</span></span> <span data-ttu-id="752aa-118">COM 類別的介面應該分割成可管理且一致的方法集合。</span><span class="sxs-lookup"><span data-stu-id="752aa-118">The interfaces of a COM class should be divided into manageable, cohesive sets of methods.</span></span>

<span data-ttu-id="752aa-119">COM 介面是不可變的;COM 合約指出無法修改它們。</span><span class="sxs-lookup"><span data-stu-id="752aa-119">COM interfaces are immutable; the COM contract states that they cannot be modified.</span></span> <span data-ttu-id="752aa-120">任何修改 (例如新增方法) 都需要定義新的介面。</span><span class="sxs-lookup"><span data-stu-id="752aa-120">Any modification (such as adding methods) requires defining a new interface.</span></span>

</dd> <dt>

<span data-ttu-id="752aa-121"><span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*COM 方法*</span><span class="sxs-lookup"><span data-stu-id="752aa-121"><span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*COM method*</span></span>
</dt> <dd>

<span data-ttu-id="752aa-122">COM 介面所提供的一組相關函數之一。</span><span class="sxs-lookup"><span data-stu-id="752aa-122">One of a set of related functions provided by a COM interface.</span></span>

</dd> </dl>

## <a name="configured-and-unconfigured-components"></a><span data-ttu-id="752aa-123">已設定和未設定的元件</span><span class="sxs-lookup"><span data-stu-id="752aa-123">Configured and Unconfigured Components</span></span>

<span data-ttu-id="752aa-124">為了充分利用 COM + 應用程式所支援的服務，COM + 環境會針對 com + 應用程式所建立的 COM 元件強加特定需求。</span><span class="sxs-lookup"><span data-stu-id="752aa-124">To take advantage of the services that COM+ applications support, the COM+ environment imposes specific requirements on COM components built for COM+ applications.</span></span> <span data-ttu-id="752aa-125">當將 COM 元件加入至 COM + 應用程式時，就稱為 *已設定的元件*。</span><span class="sxs-lookup"><span data-stu-id="752aa-125">When added to a COM+ application, a COM component is known as a *configured component*.</span></span>

<span data-ttu-id="752aa-126">針對 COM + 應用程式所建立的 COM 元件是同進程伺服器元件。</span><span class="sxs-lookup"><span data-stu-id="752aa-126">COM components built for COM+ applications are in-process server components.</span></span> <span data-ttu-id="752aa-127">元件必須包含類型程式庫 ( .tlb 檔) 來描述在元件中實建的所有類別，並在元件的所有類別上宣告介面。</span><span class="sxs-lookup"><span data-stu-id="752aa-127">The component must contain a type library (.tlb file) to describe all classes implemented in the component and declare the interfaces on all classes in the component.</span></span> <span data-ttu-id="752aa-128">您可以使用 Microsoft Visual Basic、Microsoft Visual C++ 或任何 COM 相容開發工具來建立及執行這些元件。</span><span class="sxs-lookup"><span data-stu-id="752aa-128">You can create and implement these components with Microsoft Visual Basic, Microsoft Visual C++, or any COM-compatible development tool.</span></span>

<span data-ttu-id="752aa-129">未設定的 *元件* 是未安裝在 com + 應用程式中的元件。</span><span class="sxs-lookup"><span data-stu-id="752aa-129">An *unconfigured component* is a component that isn't installed in a COM+ application.</span></span> <span data-ttu-id="752aa-130">您可以藉由將大部分未設定的元件整合至 COM + 應用程式，將這些元件轉換成已設定的元件。</span><span class="sxs-lookup"><span data-stu-id="752aa-130">You can transform most unconfigured components into configured components simply by integrating them into a COM+ application.</span></span>

> [!Note]  
> <span data-ttu-id="752aa-131">針對 COM + 應用程式和登錄中未設定的元件，請勿使用相同的 AppID。</span><span class="sxs-lookup"><span data-stu-id="752aa-131">Do not use the same AppID for both a COM+ application and in the registry for an unconfigured component.</span></span> <span data-ttu-id="752aa-132">啟用未設定的元件時，當啟用時，可能會從登錄中取得 COM 啟用所需資訊的 COM + 應用程式資訊。</span><span class="sxs-lookup"><span data-stu-id="752aa-132">When the unconfigured component is activated , as activation may retrieve the COM+ application information from the registry that does not contain the information required for COM activation.</span></span> <span data-ttu-id="752aa-133">如果從裝載 COM + 伺服器應用程式的 Dllhost.exe 呼叫 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) ，可能會發生類似的問題。</span><span class="sxs-lookup"><span data-stu-id="752aa-133">Similar problems could arise if a call is made to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) from DllHost that hosts COM+ Server application.</span></span>

 

 

 
