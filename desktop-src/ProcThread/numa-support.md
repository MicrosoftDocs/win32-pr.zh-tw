---
description: 傳統的多處理器支援模型是 (SMP) 的對稱多處理器。 在此模型中，每個處理器都有相當於記憶體和 i/o 的存取權。 隨著新增更多處理器，處理器匯流排會成為系統效能的限制。
ms.assetid: a1263968-2b26-45cc-bdd7-6aa354821a5a
title: NUMA 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178f53c6b55b6ae291cd5cdcf99386515a441094
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549803"
---
# <a name="numa-support"></a>NUMA 支援

傳統的多處理器支援模型是 (SMP) 的對稱多處理器。 在此模型中，每個處理器都有相當於記憶體和 i/o 的存取權。 隨著新增更多處理器，處理器匯流排會成為系統效能的限制。

系統設計人員使用非統一記憶體存取 (NUMA) 來提高處理器速度，而不會增加處理器匯流排的負載。 架構是非統一的，因為每個處理器都靠近記憶體的某些部分，而從記憶體的其他部分更遠。 處理器可以快速存取接近的記憶體，但需要較長的時間才能存取離離的記憶體。

在 NUMA 系統中，Cpu 會以較小的系統（稱為 *節點*）排列。 每個節點都有自己的處理器和記憶體，並透過快取一致的互連匯流排連接到較大的系統。

系統會嘗試在與所用記憶體相同的節點中，排程處理器上的執行緒，藉以改善效能。 它會嘗試滿足來自節點內的記憶體配置要求，但視需要從其他節點配置記憶體。 它也會提供 API，讓應用程式可以使用系統的拓撲。 您可以使用 NUMA 函數將排程和記憶體使用量優化，以改善應用程式的效能。

首先，您必須判斷系統中節點的版面配置。 若要取出系統中最高的編號節點，請使用 [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber) 函數。 請注意，此數目不保證等於系統中的節點總數。 此外，具有連續數位的節點不保證會同時關閉。 若要取出系統上的處理器清單，請使用 [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) 函數。 您可以使用 [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode) 函式來判斷清單中每個處理器的節點。 或者，若要取得節點中所有處理器的清單，請使用 [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask) 函數。

確定哪些處理器屬於哪些節點之後，您就可以將應用程式的效能優化。 若要確保進程的所有線程都在相同的節點上執行，請使用 [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) 函式搭配處理常式親和性遮罩，以指定相同節點中的處理器。 這會增加執行緒需要存取相同記憶體的應用程式效率。 或者，若要限制每個節點上的執行緒數目，請使用 [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) 函數。

需要海量儲存體的應用程式必須將記憶體使用量優化。 若要取出可供節點使用的可用記憶體數量，請使用 [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode) 函數。 [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)函數可讓應用程式指定記憶體配置的慣用節點。 **VirtualAllocExNuma** 不會配置任何實體頁面，因此無論這些頁面是否可在該節點上或在系統中的其他位置上，都將會成功。 實體頁面會依需求配置。 如果慣用的節點用盡頁面，記憶體管理員將會使用來自其他節點的頁面。 如果記憶體已分頁，則會在重新進入時使用相同的進程。

### <a name="numa-support-on-systems-with-more-than-64-logical-processors"></a>超過64個邏輯處理器的系統上的 NUMA 支援

在具有超過64個邏輯處理器的系統上，會根據節點的容量將節點指派給 [處理器群組](processor-groups.md) 。 節點的容量是指當系統啟動時，系統會與任何可在系統執行時新增的其他邏輯處理器一起出現的處理器數目。

**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援處理器群組。

每個節點都必須完全包含在群組內。 如果節點的容量相對較小，系統會將多個節點指派給相同群組，選擇實體接近另一個節點的節點，以獲得更佳的效能。 如果節點的容量超過群組中的處理器數目上限，系統會將節點分割成多個較小的節點，每個節點的大小都足以容納在群組中。

建立程式時，您可以使用處理 [**\_ 執行緒 \_ 屬性 \_ 慣用 \_ 節點**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) 擴充屬性來要求新進程的理想 NUMA 節點。 就像執行緒理想的處理器一樣，理想的節點是排程器的提示，可在可能的情況下，將新的進程指派給包含要求之節點的群組。

擴充 NUMA 函式 [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)、 [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)、 [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)和 [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex) 與其 unextended 對應專案不同，因為節點編號是 **USHORT** 值而不是 **UCHAR**，以容納有超過64個邏輯處理器的系統上可能有更多節點數目。 此外，由擴充函式指定或抓取的處理器包含處理器群組;unextended 函式所指定或抓取的處理器是群組相關的。 如需詳細資訊，請參閱個別的函數參考主題。

群組感知的應用程式可以使用對應的擴充 NUMA 函式，以類似于本主題稍早所述的方式，將其所有線程指派給特定的節點。 應用程式會使用 [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) 取得系統上的所有處理器清單。 請注意，除非將進程指派給單一群組，且預期的節點位於該群組中，否則應用程式無法設定進程親和性遮罩。 應用程式通常必須呼叫 [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity) ，以將其執行緒限制為預定的節點。


### <a name="behavior-starting-with-windows-10-build-20348"></a>從 Windows 10 組建20348開始的行為 

> [!NOTE]
> 從 Windows 10 組建20348開始，此和其他 NUMA 函式的行為已經過修改，可提供更好的支援系統，其節點包含更多的64處理器。

建立「假」節點以容納群組和節點之間的1:1 對應，會產生令人困惑的行為，其中報告了非預期的 NUMA 節點數目，因此從 Windows 10 組建20348開始，作業系統已變更為允許多個群組與節點相關聯，因此現在可以報告系統的真正 NUMA 拓撲。  

在對 OS 進行這些變更的過程中，有一些 NUMA Api 已變更為支援報告多個群組，而現在可以與單一 NUMA 節點相關聯。 更新和新的 Api 會標示在以下 **NUMA API** 區段的表格中。

由於移除節點分割可能會影響現有的應用程式，因此可以使用登錄值來選擇回到舊版節點分割行為。 您可以建立名為 "SplitLargeNodes" 的 **REG_DWORD** 值，並將值1放在 HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\NUMA 下方，以重新啟用節點分割。 變更此設定需要重新開機才會生效。

```powershell
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\NUMA" /v SplitLargeNumaNodes /t REG_DWORD /v 1
```

> [!NOTE]
> 如果應用程式已更新為使用新的 API 功能來回報真正的 NUMA 拓撲，在使用此登錄機碼重新啟用大型節點分割的系統上，將會繼續正常運作。

下列範例會先示範組建資料表使用舊版親和性 Api 將處理器對應到 NUMA 節點的潛在問題，而不再提供系統中所有處理器的完整涵蓋，這可能會導致不完整的資料表。 這類不完整性的含意取決於資料表的內容。 如果資料表只是儲存對應的節點編號，則這可能只是因為未發現的處理器被保留在節點0中的效能問題。 但是，如果資料表包含每個節點內容結構的指標，則會在執行時間產生 Null 取值。

接下來，此程式碼範例說明這兩個問題的因應措施。 第一個是遷移至多重群組節點親和性 Api， (使用者模式和核心模式) 。 第二種方式是使用 **KeQueryLogicalProcessorRelationship** 來直接查詢與指定處理器編號相關聯的 NUMA 節點。

```cpp

//
// Problematic implementation using KeQueryNodeActiveAffinity.
//

USHORT CurrentNode;
USHORT HighestNodeNumber;
GROUP_AFFINITY NodeAffinity;
ULONG ProcessorIndex;
PROCESSOR_NUMBER ProcessorNumber;

HighestNodeNumber = KeQueryHighestNodeNumber();
for (CurrentNode = 0; CurrentNode <= HighestNodeNumber; CurrentNode += 1) {

    KeQueryNodeActiveAffinity(CurrentNode, &NodeAffinity, NULL);
    while (NodeAffinity.Mask != 0) {

        ProcessorNumber.Group = NodeAffinity.Group;
        BitScanForward(&ProcessorNumber.Number, NodeAffinity.Mask);

        ProcessorIndex = KeGetProcessorIndexFromNumber(&ProcessorNumber);

        ProcessorNodeContexts[ProcessorIndex] = NodeContexts[CurrentNode;]

        NodeAffinity.Mask &= ~((KAFFINITY)1 << ProcessorNumber.Number);
    }
}

//
// Resolution using KeQueryNodeActiveAffinity2.
//

USHORT CurrentIndex;
USHORT CurrentNode;
USHORT CurrentNodeAffinityCount;
USHORT HighestNodeNumber;
ULONG MaximumGroupCount;
PGROUP_AFFINITY NodeAffinityMasks;
ULONG ProcessorIndex;
PROCESSOR_NUMBER ProcessorNumber;
NTSTATUS Status;

MaximumGroupCount = KeQueryMaximumGroupCount();
NodeAffinityMasks = ExAllocatePool2(POOL_FLAG_PAGED,
                                    sizeof(GROUP_AFFINITY) * MaximumGroupCount,
                                    'tseT');

if (NodeAffinityMasks == NULL) {
    return STATUS_NO_MEMORY;
}

HighestNodeNumber = KeQueryHighestNodeNumber();
for (CurrentNode = 0; CurrentNode <= HighestNodeNumber; CurrentNode += 1) {

    Status = KeQueryNodeActiveAffinity2(CurrentNode,
                                        NodeAffinityMasks,
                                        MaximumGroupCount,
                                        &CurrentNodeAffinityCount);
    NT_ASSERT(NT_SUCCESS(Status));

    for (CurrentIndex = 0; CurrentIndex < CurrentNodeAffinityCount; CurrentIndex += 1) {

        CurrentAffinity = &NodeAffinityMasks[CurrentIndex];

        while (CurrentAffinity->Mask != 0) {

            ProcessorNumber.Group = CurrentAffinity.Group;
            BitScanForward(&ProcessorNumber.Number, CurrentAffinity->Mask);

            ProcessorIndex = KeGetProcessorIndexFromNumber(&ProcessorNumber);

            ProcessorNodeContexts[ProcessorIndex] = NodeContexts[CurrentNode];

            CurrentAffinity->Mask &= ~((KAFFINITY)1 << ProcessorNumber.Number);
        }
    }
}

//
// Resolution using KeQueryLogicalProcessorRelationship.
//

ULONG ProcessorCount;
ULONG ProcessorIndex;
SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX ProcessorInformation;
ULONG ProcessorInformationSize;
PROCESSOR_NUMBER ProcessorNumber;
NTSTATUS Status;

ProcessorCount = KeQueryActiveProcessorCountEx(ALL_PROCESSOR_GROUPS);

for (ProcessorIndex = 0; ProcessorIndex < ProcessorCount; ProcessorIndex += 1) {

    Status = KeGetProcessorNumberFromIndex(ProcessorIndex, &ProcessorNumber);
    NT_ASSERT(NT_SUCCESS(Status));

    ProcessorInformationSize = sizeof(ProcessorInformation);
    Status = KeQueryLogicalProcessorRelationship(&ProcessorNumber,
                                                    RelationNumaNode,
                                                    &ProcessorInformation,
                                                    &ProcesorInformationSize);
    NT_ASSERT(NT_SUCCESS(Status));

    NodeNumber = ProcessorInformation.NumaNode.NodeNumber;

    ProcessorNodeContexts[ProcessorIndex] = NodeContexts[NodeNumber];
}
```

## <a name="numa-api"></a>NUMA API

下表描述 NUMA API。



| 函式                                                                     | 描述                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)      | 配置要在指定進程 (AWE) 區域內的任何 [位址視窗擴充](../memory/address-windowing-extensions.md) 內對應和取消對應的實體記憶體頁面，並為實體記憶體指定 NUMA 節點。 |
| [**CreateFileMappingNuma**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingnumaw)                      | 針對指定的檔案建立或開啟已命名或未命名的檔案對應物件，並為實體記憶體指定 NUMA 節點。                                                                                              |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | 已在 Windows 10 組建20348中更新。 抓取邏輯處理器和相關硬體的相關資訊。                                                                                                                                                            |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | 已在 Windows 10 組建20348中更新。 抓取邏輯處理器和相關硬體關聯性的相關資訊。                                                                                                                                       |
| [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)             | 抓取指定節點中的可用記憶體數量。                                                                                                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)         | 抓取指定為 **USHORT** 值之節點中的可用記憶體數量。                                                                                                                                             |
| [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)                 | 抓取目前具有最大數目的節點。                                                                                                                                                                       |
| [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)                 | 已在 Windows 10 組建20348中更新。 抓取指定節點的處理器遮罩。                                                                                                                                                                            |
| [**GetNumaNodeProcessorMask2**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormask2)                         | Windows 10 組建20348中的新功能。 抓取指定之節點的多群組處理器遮罩。                                                                                                                                                                          |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)             | 已在 Windows 10 組建20348中更新。 抓取指定為 **USHORT** 值之節點的處理器遮罩。                                                                                                                                                        |
| [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                         | 抓取指定處理器的節點編號。                                                                                                                                                                          |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                     | 以指定處理器的 **USHORT** 值形式抓取節點編號。                                                                                                                                                    |
| [**GetNumaProximityNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                         | 抓取指定的相近識別碼的節點編號。                                                                                                                                                               |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                     | 將節點編號抓取為指定之相近識別碼的 **USHORT** 值。                                                                                                                                         |
| [**GetProcessDefaultCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessdefaultcpusetmasks)                     | Windows 10 組建20348中的新功能。 抓取 SetProcessDefaultCpuSetMasks 或 SetProcessDefaultCpuSets 所設定之進程預設集中的 CPU 集合清單。                                                                                                                                         |
| [**GetThreadSelectedCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadselectedcpusetmasks)                     | Windows 10 組建20348中的新功能。 為指定的執行緒設定選取的 CPU 集合指派。 此指派會覆寫進程預設指派（如果有設定）。                                                                                                                                          |
| [**MapViewOfFileExNuma**](/windows/win32/api/winbase/nf-winbase-mapviewoffileexnuma)                          | 將檔案對應的視圖對應至呼叫進程的位址空間，並為實體記憶體指定 NUMA 節點。                                                                                                 |
| [**SetProcessDefaultCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessdefaultcpusetmasks)                     | Windows 10 組建20348中的新功能。 針對指定進程中的執行緒，設定預設的 CPU 集合指派。                                                                                                                                          |
| [**SetThreadSelectedCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadselectedcpusetmasks)                     | Windows 10 組建20348中的新功能。 為指定的執行緒設定選取的 CPU 集合指派。 此指派會覆寫進程預設指派（如果有設定）。                                                                                                                                          |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                            | 保留或認可指定進程的虛擬位址空間內的記憶體區域，並指定實體記憶體的 NUMA 節點。                                                                          |



 

[**QueryWorkingSetEx**](/windows/win32/api/psapi/nf-psapi-queryworkingsetex)函式可用來取出配置頁面的 NUMA 節點。 如需範例，請參閱 [從 NUMA 節點配置記憶體](../memory/allocating-memory-from-a-numa-node.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[從 NUMA 節點配置記憶體](../memory/allocating-memory-from-a-numa-node.md)
</dt> <dt>

[多個處理器](multiple-processors.md)
</dt> <dt>

[處理器群組](processor-groups.md)
</dt> </dl>

 

 
