---
description: 這個類別是網路事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: afa994ef-dd1c-4909-a6cd-7021be4fff40
title: SystemConfig_Network 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Network
- SystemConfig_Network.TcbTablePartitions
- SystemConfig_Network.MaxHashTableSize
- SystemConfig_Network.MaxUserPort
- SystemConfig_Network.TcpTimedWaitDelay
api_type:
- NA
api_location: ''
ms.openlocfilehash: 23b469c31645c6a5b04319f91b758ee19beb935c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972164"
---
# <a name="systemconfig_network-class"></a><span data-ttu-id="c66ef-104">SystemConfig \_ Network 類別</span><span class="sxs-lookup"><span data-stu-id="c66ef-104">SystemConfig\_Network class</span></span>

<span data-ttu-id="c66ef-105">這個類別是網路事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="c66ef-105">This class is the event type class for network events.</span></span>

<span data-ttu-id="c66ef-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="c66ef-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c66ef-107">語法</span><span class="sxs-lookup"><span data-stu-id="c66ef-107">Syntax</span></span>

``` syntax
[EventType(17), EventTypeName("Network")]
class SystemConfig_Network : SystemConfig
{
  uint32 TcbTablePartitions;
  uint32 MaxHashTableSize;
  uint32 MaxUserPort;
  uint32 TcpTimedWaitDelay;
};
```

## <a name="members"></a><span data-ttu-id="c66ef-108">成員</span><span class="sxs-lookup"><span data-stu-id="c66ef-108">Members</span></span>

<span data-ttu-id="c66ef-109">**SystemConfig \_ Network** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c66ef-109">The **SystemConfig\_Network** class has these types of members:</span></span>

-   [<span data-ttu-id="c66ef-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c66ef-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c66ef-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c66ef-111">Properties</span></span>

<span data-ttu-id="c66ef-112">**SystemConfig \_ Network** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c66ef-112">The **SystemConfig\_Network** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c66ef-113">**MaxHashTableSize**</span><span class="sxs-lookup"><span data-stu-id="c66ef-113">**MaxHashTableSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c66ef-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c66ef-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c66ef-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c66ef-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c66ef-116">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="c66ef-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="c66ef-117">儲存 (TCBs) 之 TCP 控制區塊的雜湊表大小。</span><span class="sxs-lookup"><span data-stu-id="c66ef-117">The size of the hash table in which TCP control blocks (TCBs) are stored.</span></span> <span data-ttu-id="c66ef-118">TCP 會將控制區塊儲存在雜湊表中，以便快速找到它們。</span><span class="sxs-lookup"><span data-stu-id="c66ef-118">TCP stores control blocks in a hash table so it can find them very quickly.</span></span>

</dd> <dt>

<span data-ttu-id="c66ef-119">**MaxUserPort**</span><span class="sxs-lookup"><span data-stu-id="c66ef-119">**MaxUserPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c66ef-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c66ef-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c66ef-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c66ef-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c66ef-122">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="c66ef-122">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="c66ef-123">當應用程式向系統要求可用的使用者埠時，TCP 可指派的最高埠號碼。</span><span class="sxs-lookup"><span data-stu-id="c66ef-123">The highest port number TCP can assign when an application requests an available user port from the system.</span></span> <span data-ttu-id="c66ef-124">一般來說，短暫) 的暫時埠 (會配置給埠號碼1024到5000。</span><span class="sxs-lookup"><span data-stu-id="c66ef-124">Typically, ephemeral ports (those used briefly) are allocated to port numbers 1024 through 5000.</span></span>

<span data-ttu-id="c66ef-125">TCP 可指派的最高使用者埠號碼值是由登錄設定所控制。</span><span class="sxs-lookup"><span data-stu-id="c66ef-125">The value for the highest user port number TCP can assign is controlled by a registry setting.</span></span> <span data-ttu-id="c66ef-126">如需詳細資訊，請參閱 [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10))。</span><span class="sxs-lookup"><span data-stu-id="c66ef-126">For more information, see [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).</span></span>

</dd> <dt>

<span data-ttu-id="c66ef-127">**TcbTablePartitions**</span><span class="sxs-lookup"><span data-stu-id="c66ef-127">**TcbTablePartitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c66ef-128">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c66ef-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c66ef-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c66ef-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c66ef-130">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="c66ef-130">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="c66ef-131">傳輸控制區塊資料表中的資料分割數目。</span><span class="sxs-lookup"><span data-stu-id="c66ef-131">The number of partitions in the Transport Control Block table.</span></span> <span data-ttu-id="c66ef-132">分割傳輸控制區塊資料表可將資料表存取的爭用降至最低。</span><span class="sxs-lookup"><span data-stu-id="c66ef-132">Partitioning the Transport Control Block table minimizes contention for table access.</span></span> <span data-ttu-id="c66ef-133">這在多處理器系統上特別有用。</span><span class="sxs-lookup"><span data-stu-id="c66ef-133">This is especially useful on multiprocessor systems.</span></span>

</dd> <dt>

<span data-ttu-id="c66ef-134">**TcpTimedWaitDelay**</span><span class="sxs-lookup"><span data-stu-id="c66ef-134">**TcpTimedWaitDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c66ef-135">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c66ef-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c66ef-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c66ef-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c66ef-137">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="c66ef-137">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="c66ef-138">必須經過多久的時間，TCP 才能釋放關閉的連線並重複使用其資源。</span><span class="sxs-lookup"><span data-stu-id="c66ef-138">The time that must elapse before TCP can release a closed connection and reuse its resources.</span></span> <span data-ttu-id="c66ef-139">結束和釋放之間的此間隔稱為「 \_ 等候狀態」或「2MSL」狀態。</span><span class="sxs-lookup"><span data-stu-id="c66ef-139">This interval between closure and release is known as the TIME\_WAIT state or 2MSL state.</span></span> <span data-ttu-id="c66ef-140">在這段期間內，您可以在用戶端和伺服器之間重新開啟連接，而不需要建立新的連接。</span><span class="sxs-lookup"><span data-stu-id="c66ef-140">During this time, the connection can be reopened at much less cost to the client and server than establishing a new connection.</span></span>

<span data-ttu-id="c66ef-141">IETF 所發佈的 RFC 793，會要求 TCP 將間隔維持在至少等於最大區段存留期 (2MSL) 網路的間隔。</span><span class="sxs-lookup"><span data-stu-id="c66ef-141">RFC 793 published by the IETF requires that TCP maintains a closed connection for an interval at least equal to twice the maximum segment lifetime (2MSL) of the network.</span></span> <span data-ttu-id="c66ef-142">當連接釋出時，其通訊端配對和 TCP 控制區塊 (TCB) 可用來支援另一個連線。</span><span class="sxs-lookup"><span data-stu-id="c66ef-142">When a connection is released, its socket pair and TCP control block (TCB) can be used to support another connection.</span></span> <span data-ttu-id="c66ef-143">根據預設，MSL 定義為120秒，而此專案的值等於兩個 Msls.contentitem 或4分鐘。</span><span class="sxs-lookup"><span data-stu-id="c66ef-143">By default, the MSL is defined to be 120 seconds, and the value of this entry is equal to two MSLs, or 4 minutes.</span></span> <span data-ttu-id="c66ef-144">如需詳細資訊，請參閱 [RFC 793](https://tools.ietf.org/html/rfc973)。</span><span class="sxs-lookup"><span data-stu-id="c66ef-144">For more information, see [RFC 793](https://tools.ietf.org/html/rfc973).</span></span>

<span data-ttu-id="c66ef-145">使用登錄設定來縮減這個專案的值，可讓 TCP 更快釋放關閉的連線，為新的連接提供更多資源。</span><span class="sxs-lookup"><span data-stu-id="c66ef-145">Reducing the value of this entry using a registry setting allows TCP to release closed connections faster, providing more resources for new connections.</span></span> <span data-ttu-id="c66ef-146">但是，如果值太低，TCP 可能會在連接完成之前釋出連線資源，要求伺服器使用額外的資源來重新建立連接。</span><span class="sxs-lookup"><span data-stu-id="c66ef-146">However, if the value is too low, TCP might release connection resources before the connection is complete, requiring the server to use additional resources to reestablish the connection.</span></span>

<span data-ttu-id="c66ef-147">一般來說，TCP 不會釋放關閉的連線，直到這個專案的值到期為止。</span><span class="sxs-lookup"><span data-stu-id="c66ef-147">Normally, TCP does not release closed connections until the value of this entry expires.</span></span> <span data-ttu-id="c66ef-148">但是，如果 (TCBs) ，TCP 會在此值過期之前釋放連接。</span><span class="sxs-lookup"><span data-stu-id="c66ef-148">However, TCP can release connections before this value expires if it is running out of TCP control blocks (TCBs).</span></span> <span data-ttu-id="c66ef-149">系統所建立的 TCBs 數目是由登錄設定所控制。</span><span class="sxs-lookup"><span data-stu-id="c66ef-149">The number of TCBs the system creates is controlled by a registry setting.</span></span> <span data-ttu-id="c66ef-150">如需詳細資訊，請參閱 [MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10))。</span><span class="sxs-lookup"><span data-stu-id="c66ef-150">For more information, see [MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c66ef-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="c66ef-151">Requirements</span></span>



| <span data-ttu-id="c66ef-152">需求</span><span class="sxs-lookup"><span data-stu-id="c66ef-152">Requirement</span></span> | <span data-ttu-id="c66ef-153">值</span><span class="sxs-lookup"><span data-stu-id="c66ef-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c66ef-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c66ef-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c66ef-155">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c66ef-155">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c66ef-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c66ef-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c66ef-157">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c66ef-157">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c66ef-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c66ef-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c66ef-159">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="c66ef-159">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 
