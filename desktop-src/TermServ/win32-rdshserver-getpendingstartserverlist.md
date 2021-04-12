---
title: Win32_RDSHServer 類別的 GetPendingStartServerList 方法
description: 抓取等候啟動的伺服器清單。
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- GetPendingStartServerList 方法遠端桌面服務
- GetPendingStartServerList 方法遠端桌面服務，Win32_RDSHServer 類別
- Win32_RDSHServer 類別遠端桌面服務，GetPendingStartServerList 方法
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetPendingStartServerList
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b96453b33f931b18d89f13413513d3baf82bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384757"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="f3635-106">Win32 RDSHServer 類別的 GetPendingStartServerList 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f3635-106">GetPendingStartServerList method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="f3635-107">抓取等候啟動的伺服器清單。</span><span class="sxs-lookup"><span data-stu-id="f3635-107">Retrieves a list of server waiting to start.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3635-108">語法</span><span class="sxs-lookup"><span data-stu-id="f3635-108">Syntax</span></span>


```mof
uint32 GetPendingStartServerList(
  [in]  uint32 maxServers,
  [out] string ServerFQDNs[]
);
```



## <a name="parameters"></a><span data-ttu-id="f3635-109">參數</span><span class="sxs-lookup"><span data-stu-id="f3635-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3635-110">*maxServers* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3635-110">*maxServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3635-111">要在清單中傳回的最大伺服器數目。</span><span class="sxs-lookup"><span data-stu-id="f3635-111">The maximum number of servers to return in the list.</span></span>

</dd> <dt>

<span data-ttu-id="f3635-112">*ServerFQDNs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f3635-112">*ServerFQDNs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3635-113">成功時，會包含等待啟動之伺服器的完整功能變數名稱集合。</span><span class="sxs-lookup"><span data-stu-id="f3635-113">On success, contains a collection of fully-qualified domain names of the servers waiting to start.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3635-114">備註</span><span class="sxs-lookup"><span data-stu-id="f3635-114">Remarks</span></span>

<span data-ttu-id="f3635-115">伺服器清單會在每次呼叫之後重設，讓下一個呼叫不會收到重複的伺服器。</span><span class="sxs-lookup"><span data-stu-id="f3635-115">The list of servers is reset after every call, so that the next call will not get a duplicate server.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3635-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3635-116">Requirements</span></span>



| <span data-ttu-id="f3635-117">需求</span><span class="sxs-lookup"><span data-stu-id="f3635-117">Requirement</span></span> | <span data-ttu-id="f3635-118">值</span><span class="sxs-lookup"><span data-stu-id="f3635-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3635-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3635-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f3635-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="f3635-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f3635-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3635-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f3635-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f3635-122">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="f3635-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="f3635-123">Namespace</span></span><br/>                | <span data-ttu-id="f3635-124">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="f3635-124">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f3635-125">MOF</span><span class="sxs-lookup"><span data-stu-id="f3635-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3635-126"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3635-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3635-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f3635-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3635-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3635-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f3635-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3635-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3635-130">**Win32 \_ RDSHServer**</span><span class="sxs-lookup"><span data-stu-id="f3635-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





