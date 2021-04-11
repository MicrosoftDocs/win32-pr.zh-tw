---
title: ITSRemoteProgram2 介面
description: 定義與 RemoteApp 搭配使用的屬性。
ms.assetid: e0b6bd9f-e66b-4543-b424-7b773141b598
ms.tgt_platform: multiple
keywords:
- ITSRemoteProgram2 介面遠端桌面服務
- ITSRemoteProgram2 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- ITSRemoteProgram2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f57e78d5027d1825f9e1601eb1f36efb94d37a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934969"
---
# <a name="itsremoteprogram2-interface"></a><span data-ttu-id="5a97c-105">ITSRemoteProgram2 介面</span><span class="sxs-lookup"><span data-stu-id="5a97c-105">ITSRemoteProgram2 interface</span></span>

<span data-ttu-id="5a97c-106">定義與 RemoteApp 搭配使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="5a97c-106">Defines properties for use with a RemoteApp.</span></span>

## <a name="members"></a><span data-ttu-id="5a97c-107">成員</span><span class="sxs-lookup"><span data-stu-id="5a97c-107">Members</span></span>

<span data-ttu-id="5a97c-108">**ITSRemoteProgram2** 介面繼承自 [**ITSRemoteProgram**](itsremoteprogram.md)。</span><span class="sxs-lookup"><span data-stu-id="5a97c-108">The **ITSRemoteProgram2** interface inherits from [**ITSRemoteProgram**](itsremoteprogram.md).</span></span> <span data-ttu-id="5a97c-109">**ITSRemoteProgram2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5a97c-109">**ITSRemoteProgram2** also has these types of members:</span></span>

-   [<span data-ttu-id="5a97c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="5a97c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5a97c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="5a97c-111">Properties</span></span>

<span data-ttu-id="5a97c-112">**ITSRemoteProgram2** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5a97c-112">The **ITSRemoteProgram2** interface has these properties.</span></span>



| <span data-ttu-id="5a97c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="5a97c-113">Property</span></span>                                                                                  | <span data-ttu-id="5a97c-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="5a97c-114">Access type</span></span>           | <span data-ttu-id="5a97c-115">Description</span><span class="sxs-lookup"><span data-stu-id="5a97c-115">Description</span></span>                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------|
| [<span data-ttu-id="5a97c-116">**RemoteApplicationArgs**</span><span class="sxs-lookup"><span data-stu-id="5a97c-116">**RemoteApplicationArgs**</span></span>](itsremoteprogram2-remoteapplicationargs.md)<br/>       | <span data-ttu-id="5a97c-117">唯寫</span><span class="sxs-lookup"><span data-stu-id="5a97c-117">Write-only</span></span><br/> | <span data-ttu-id="5a97c-118">RemoteApp 的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="5a97c-118">The command-line arguments for the RemoteApp.</span></span><br/>    |
| [<span data-ttu-id="5a97c-119">**RemoteApplicationName**</span><span class="sxs-lookup"><span data-stu-id="5a97c-119">**RemoteApplicationName**</span></span>](itsremoteprogram2-remoteapplicationname.md)<br/>       | <span data-ttu-id="5a97c-120">唯寫</span><span class="sxs-lookup"><span data-stu-id="5a97c-120">Write-only</span></span><br/> | <span data-ttu-id="5a97c-121">RemoteApp 的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a97c-121">The name of the RemoteApp.</span></span><br/>                       |
| [<span data-ttu-id="5a97c-122">**RemoteApplicationProgram**</span><span class="sxs-lookup"><span data-stu-id="5a97c-122">**RemoteApplicationProgram**</span></span>](itsremoteprogram2-remoteapplicationprogram.md)<br/> | <span data-ttu-id="5a97c-123">唯寫</span><span class="sxs-lookup"><span data-stu-id="5a97c-123">Write-only</span></span><br/> | <span data-ttu-id="5a97c-124">RemoteApp 程式的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="5a97c-124">The path and file name of the RemoteApp program.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5a97c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a97c-125">Requirements</span></span>



| <span data-ttu-id="5a97c-126">需求</span><span class="sxs-lookup"><span data-stu-id="5a97c-126">Requirement</span></span> | <span data-ttu-id="5a97c-127">值</span><span class="sxs-lookup"><span data-stu-id="5a97c-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a97c-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a97c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5a97c-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5a97c-129">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="5a97c-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a97c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5a97c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a97c-131">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5a97c-132">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5a97c-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="5a97c-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a97c-133"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a97c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5a97c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a97c-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a97c-135"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a97c-136">IID</span><span class="sxs-lookup"><span data-stu-id="5a97c-136">IID</span></span><br/>                      | <span data-ttu-id="5a97c-137">IID \_ ITSRemoteProgram2 定義為92C38A7D-241A-418c-9936-099872C9AF20</span><span class="sxs-lookup"><span data-stu-id="5a97c-137">IID\_ITSRemoteProgram2 is defined as 92C38A7D-241A-418c-9936-099872C9AF20</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="5a97c-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a97c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a97c-139">**ITSRemoteProgram**</span><span class="sxs-lookup"><span data-stu-id="5a97c-139">**ITSRemoteProgram**</span></span>](itsremoteprogram.md)
</dt> </dl>

 

 





