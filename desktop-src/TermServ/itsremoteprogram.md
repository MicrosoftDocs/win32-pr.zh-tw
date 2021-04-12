---
title: ITSRemoteProgram 介面
description: 包含用來設定和取出 remoteapp 模式的方法，以及 RemoteApp 程式的啟動參數，例如可執行檔和工作目錄的路徑。
ms.assetid: c9eec63b-7162-4bf8-b5d5-8cadb971ef98
ms.tgt_platform: multiple
keywords:
- ITSRemoteProgram 介面遠端桌面服務
- ITSRemoteProgram 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- ITSRemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfec99c109dfd3f69e22caf13071b77cd41f61bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025237"
---
# <a name="itsremoteprogram-interface"></a><span data-ttu-id="40ee9-105">ITSRemoteProgram 介面</span><span class="sxs-lookup"><span data-stu-id="40ee9-105">ITSRemoteProgram interface</span></span>

<span data-ttu-id="40ee9-106">包含用來設定和取出 remoteapp 模式的方法，以及 RemoteApp 程式的啟動參數，例如可執行檔和工作目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="40ee9-106">Includes methods to set and retrieve the RemoteApp mode and the start-up parameters for a RemoteApp program, such as the path of the executable file and the working directory.</span></span>

## <a name="members"></a><span data-ttu-id="40ee9-107">成員</span><span class="sxs-lookup"><span data-stu-id="40ee9-107">Members</span></span>

<span data-ttu-id="40ee9-108">**ITSRemoteProgram** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="40ee9-108">The **ITSRemoteProgram** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="40ee9-109">**ITSRemoteProgram** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="40ee9-109">**ITSRemoteProgram** also has these types of members:</span></span>

-   [<span data-ttu-id="40ee9-110">方法</span><span class="sxs-lookup"><span data-stu-id="40ee9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="40ee9-111">屬性</span><span class="sxs-lookup"><span data-stu-id="40ee9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="40ee9-112">方法</span><span class="sxs-lookup"><span data-stu-id="40ee9-112">Methods</span></span>

<span data-ttu-id="40ee9-113">**ITSRemoteProgram** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="40ee9-113">The **ITSRemoteProgram** interface has these methods.</span></span>



| <span data-ttu-id="40ee9-114">方法</span><span class="sxs-lookup"><span data-stu-id="40ee9-114">Method</span></span>                                                            | <span data-ttu-id="40ee9-115">描述</span><span class="sxs-lookup"><span data-stu-id="40ee9-115">Description</span></span>                                                              |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="40ee9-116">**ServerStartProgram**</span><span class="sxs-lookup"><span data-stu-id="40ee9-116">**ServerStartProgram**</span></span>](itsremoteprogram-serverstartprogram.md) | <span data-ttu-id="40ee9-117">指定要在遠端會話中啟動的 RemoteApp 程式。</span><span class="sxs-lookup"><span data-stu-id="40ee9-117">Specifies a RemoteApp program to start in the remote session.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="40ee9-118">屬性</span><span class="sxs-lookup"><span data-stu-id="40ee9-118">Properties</span></span>

<span data-ttu-id="40ee9-119">**ITSRemoteProgram** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="40ee9-119">The **ITSRemoteProgram** interface has these properties.</span></span>



| <span data-ttu-id="40ee9-120">屬性</span><span class="sxs-lookup"><span data-stu-id="40ee9-120">Property</span></span>                                                                   | <span data-ttu-id="40ee9-121">存取類型</span><span class="sxs-lookup"><span data-stu-id="40ee9-121">Access type</span></span>           | <span data-ttu-id="40ee9-122">Description</span><span class="sxs-lookup"><span data-stu-id="40ee9-122">Description</span></span>                    |
|:---------------------------------------------------------------------------|:----------------------|:-------------------------------|
| [<span data-ttu-id="40ee9-123">**RemoteProgramMode**</span><span class="sxs-lookup"><span data-stu-id="40ee9-123">**RemoteProgramMode**</span></span>](itsremoteprogram-remoteprogrammode.md)<br/> | <span data-ttu-id="40ee9-124">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="40ee9-124">Read/write</span></span><br/> | <span data-ttu-id="40ee9-125">RemoteApp 模式。</span><span class="sxs-lookup"><span data-stu-id="40ee9-125">The RemoteApp mode.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="40ee9-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="40ee9-126">Requirements</span></span>



| <span data-ttu-id="40ee9-127">需求</span><span class="sxs-lookup"><span data-stu-id="40ee9-127">Requirement</span></span> | <span data-ttu-id="40ee9-128">值</span><span class="sxs-lookup"><span data-stu-id="40ee9-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40ee9-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40ee9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="40ee9-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40ee9-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="40ee9-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40ee9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="40ee9-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40ee9-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="40ee9-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="40ee9-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="40ee9-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40ee9-134"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="40ee9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="40ee9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40ee9-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40ee9-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="40ee9-137">IID</span><span class="sxs-lookup"><span data-stu-id="40ee9-137">IID</span></span><br/>                      | <span data-ttu-id="40ee9-138">IID \_ ITSRemoteProgram 定義為 FDD029F9-467A-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="40ee9-138">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="40ee9-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40ee9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40ee9-140">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="40ee9-140">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="40ee9-141">遠端桌面網頁連線參考</span><span class="sxs-lookup"><span data-stu-id="40ee9-141">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

