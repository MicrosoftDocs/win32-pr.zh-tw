---
title: 'CB_CONNECTION_INFO 結構 (Cbclient .h) '
description: 包含連入連線要求的相關資訊。
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- CB_CONNECTION_INFO 結構遠端桌面服務
- PCB_CONNECTION_INFO 結構指標遠端桌面服務
topic_type:
- apiref
api_name:
- CB_CONNECTION_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36370a4faa823f509d1f3356768add0ece9a6904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384213"
---
# <a name="cb_connection_info-structure"></a><span data-ttu-id="6a4ec-105">CB \_ 連接 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="6a4ec-105">CB\_CONNECTION\_INFO structure</span></span>

<span data-ttu-id="6a4ec-106">包含連入連線要求的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6a4ec-106">Contains information about an incoming connection request.</span></span> <span data-ttu-id="6a4ec-107">此結構會搭配 [**IConnectionBrokerClient：： GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) 方法使用。</span><span class="sxs-lookup"><span data-stu-id="6a4ec-107">This structure is used with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a4ec-108">語法</span><span class="sxs-lookup"><span data-stu-id="6a4ec-108">Syntax</span></span>


```C++
typedef struct {
  WCHAR            UserName[CB_USERNAME_LENGTH];
  WCHAR            Domain[CB_DOMAINNAME_LENGTH];
  WCHAR            InitialProgram[CB_INITAPP_LENGTH];
  CB_RESOURCE_TYPE Resource;
  WCHAR            PluginName[CB_PLUGINNAME_LENGTH];
  WCHAR            FarmName[CB_FARMNAME_LENGTH];
  DWORD            dwVendorInfoLength;
  PBYTE            pVendorSpecificInfo;
} CB_CONNECTION_INFO, *PCB_CONNECTION_INFO;
```



## <a name="members"></a><span data-ttu-id="6a4ec-109">成員</span><span class="sxs-lookup"><span data-stu-id="6a4ec-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="6a4ec-110">**使用者名稱**</span><span class="sxs-lookup"><span data-stu-id="6a4ec-110">**UserName**</span></span>
</dt> <dd>

<span data-ttu-id="6a4ec-111">要求會話之使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a4ec-111">The name of the user requesting a session.</span></span>

</dd> <dt>

<span data-ttu-id="6a4ec-112">**網域**</span><span class="sxs-lookup"><span data-stu-id="6a4ec-112">**Domain**</span></span>
</dt> <dd>

<span data-ttu-id="6a4ec-113">使用者 **名稱為其** 成員之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a4ec-113">The name of the domain that **UserName** is a member of.</span></span>

</dd> <dt>

<span data-ttu-id="6a4ec-114">**InitialProgram**</span><span class="sxs-lookup"><span data-stu-id="6a4ec-114">**InitialProgram**</span></span>
</dt> <dd>

<span data-ttu-id="6a4ec-115">啟動會話時啟動之初始程式的完整路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="6a4ec-115">The fully qualified path and file name of the initial program that is started when the session is started.</span></span> <span data-ttu-id="6a4ec-116">如果不應該啟動任何初始程式，請將這個成員設定為空字串。</span><span class="sxs-lookup"><span data-stu-id="6a4ec-116">Set this member to an empty string if no initial program should be started.</span></span>

</dd> <dt>

<span data-ttu-id="6a4ec-117">**Resource**</span><span class="sxs-lookup"><span data-stu-id="6a4ec-117">**Resource**</span></span>
</dt> <dd>

<span data-ttu-id="6a4ec-118">[**CB \_ 資源 \_ 類型**](cb-resource-type.md)列舉值，指定連入連接所連接的資源類型。</span><span class="sxs-lookup"><span data-stu-id="6a4ec-118">A value of the [**CB\_RESOURCE\_TYPE**](cb-resource-type.md) enumeration that specifies the type of resource that the incoming connection is connecting to.</span></span> <span data-ttu-id="6a4ec-119">如果 **PluginName** 成員為 **Null**，遠端桌面連線代理人會使用這個成員來判斷要叫用哪個外掛程式來判斷目的電腦。</span><span class="sxs-lookup"><span data-stu-id="6a4ec-119">If the **PluginName** member is **NULL**, this member is used to by the Remote Desktop Connection Broker to determine which plug-in to invoke for determining the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="6a4ec-120">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="6a4ec-120">**PluginName**</span></span>
</dt> <dd>

<span data-ttu-id="6a4ec-121">要叫用來判斷目的電腦之外掛程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a4ec-121">The name of the plug-in to invoke to determine the target computer.</span></span> <span data-ttu-id="6a4ec-122">如果此參數為 **Null**，則會使用 **資源** 成員來決定要叫用的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="6a4ec-122">If this parameter is **NULL**, the **Resource** member is used to determine which plug-in to invoke.</span></span>

</dd> <dt>

<span data-ttu-id="6a4ec-123">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="6a4ec-123">**FarmName**</span></span>
</dt> <dd>

<span data-ttu-id="6a4ec-124">包含電腦的伺服器陣列名稱稱，其中一個是將會重新導向連接的目的電腦。</span><span class="sxs-lookup"><span data-stu-id="6a4ec-124">The name of the farm that contains the computers, one of which will be the target computer where the connection will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="6a4ec-125">**dwVendorInfoLength**</span><span class="sxs-lookup"><span data-stu-id="6a4ec-125">**dwVendorInfoLength**</span></span>
</dt> <dd>

<span data-ttu-id="6a4ec-126">這個成員保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="6a4ec-126">This member is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="6a4ec-127">**pVendorSpecificInfo**</span><span class="sxs-lookup"><span data-stu-id="6a4ec-127">**pVendorSpecificInfo**</span></span>
</dt> <dd>

<span data-ttu-id="6a4ec-128">這個成員保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="6a4ec-128">This member is reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a4ec-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a4ec-129">Requirements</span></span>



| <span data-ttu-id="6a4ec-130">需求</span><span class="sxs-lookup"><span data-stu-id="6a4ec-130">Requirement</span></span> | <span data-ttu-id="6a4ec-131">值</span><span class="sxs-lookup"><span data-stu-id="6a4ec-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a4ec-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a4ec-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6a4ec-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6a4ec-133">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="6a4ec-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a4ec-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6a4ec-135">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a4ec-135">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="6a4ec-136">標頭</span><span class="sxs-lookup"><span data-stu-id="6a4ec-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a4ec-137"><dt>Cbclient。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a4ec-137"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a4ec-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a4ec-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a4ec-139">**IConnectionBrokerClient::GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="6a4ec-139">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





