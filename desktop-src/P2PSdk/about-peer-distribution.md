---
description: 對等散發 API （支援 Windows 7、Windows Server 2008 R2、Windows 8 和 Windows Server 2012 中的分支快取功能）提供了一組平臺 Api，可在從遠端辦公室存取時提高集中式應用程式的網路回應能力，並協助降低整體廣域網路 (WAN) 使用率，而不會干擾網路安全性技術。
ms.assetid: feb9666e-563a-49f4-ad1c-f166a0faff31
title: 關於對等分佈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c996aed35ac691284ba61b757d6ff5a88033aad
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120433"
---
# <a name="about-peer-distribution"></a>關於對等分佈

對等散發 API （支援 Windows 7、Windows Server 2008 R2、Windows 8 和 Windows Server 2012 中的分支快取功能）提供了一組平臺 Api，可在從遠端辦公室存取時提高集中式應用程式的網路回應能力，並協助降低整體廣域網路 (WAN) 使用率，而不會干擾網路安全性技術。

對等散發系統提供一組平臺 Api，供發行者用來提供數位內容和要求的取用者。 若要輕鬆地區分這些角色，您可以更輕鬆地將伺服器角色中的發行者和用戶端角色中的取用者想像。 除此之外，請務必記住，在這些概念角色之前，對等散發服務是真正的對等系統，這是由任何對等分佈節點發布和取用數位內容的能力所表示。 對等散發平臺 Api 是由 Win32 匯入連結 **庫 (的**) 來公開給發行者和取用者。

發行者提供的內容生命週期，由具有對等散發服務的取用者所抓取，是由下列作業所組成：



|                         | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **內容發佈** | 發佈的目的是要產生稱為 **內容資訊** 的內容描述，或簡短的 **內容資訊** 。 這項內容資訊可供對等散發服務的實例用來驗證和重建內容。 當應用程式將內容發佈至對等散發服務（在概念上是伺服器端作業）時，該內容會變成與發行者身分識別相關聯，這是以與執行緒存取權杖相關聯之使用者的 SID 為基礎。 這項系結是為了限制未經授權的實體存取內容而完成。 不過，請務必注意，內容資訊的存取相當於存取內容本身，因為內容資訊可以用來取得對等或託管快取的內容。<br/> Windows 8 中有新版本的內容資訊資料結構;不過，仍支援舊版。 若要與 Windows 7 用戶端交互操作，系統管理員可以將對等散發服務設定為使用舊版的內容資訊資料結構。<br/> |
| **內容抓取**   | 若要讓取用者從對等散發服務取得內容，必須將存取權提供給與該內容相關聯的已發佈內容資訊。 用來發佈內容的對等散發服務可以提供相關聯的內容資訊。 當取用者具有內容資訊之後，其他對等散發 Api 就可以用來向對等散發服務要求內容。 對等散發服務將嘗試從區域網路取得內容。 如果內容無法使用，用戶端應用程式會負責從來源伺服器抓取內容。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **移除發行集** | 針對已將內容發佈至對等散發服務的應用程式，已提供 [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish) 函式以允許解除發佈內容。 解除發佈內容之後，本機對等散發服務將不再提供與該內容相關聯的內容資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="asynchronous-completions"></a>非同步完成

對等散發 API 支援非同步 API 模型，因此對等散發 Api 可讓您使用 i/o 完成埠或事件作為處理非同步對等散發作業完成的信號機制。 針對任一個機制，對等分佈會使用重迭 [**的結構。**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 一般而言，對等散發會取得重 **迭結構的** 擁有權，以及用戶端傳遞給非同步 API 函式的任何 out 參數。 在特定非同步函式完成之前，用戶端不能存取這些資源。 非同步函式完成時，對等散發服務將不再需要這些資源的存取權，而且可以在呼叫的應用程式符合時重複使用。

如果函式傳回 **錯誤 \_ IO \_ 擱置** 以外的任何錯誤碼，將不會有任何非同步完成。 傳回 **錯誤 \_ IO \_ 暫** 止的值表示呼叫同步失敗。 如果對等散發 API 傳回 **錯誤 \_ IO \_ 暫** 止，則呼叫端必須等候非同步完成。

您可以透過下列兩種方式之一來抓取非同步完成的錯誤碼：

**I/o 完成埠自動完成**

使用者藉由提供完成埠控制碼和完成金鑰給下列 API 函式，來叫用 i/o 完成埠機制：

<dl>

[**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)  
[**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)  
[**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)  
[**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)  
</dl>

使用者可以藉由呼叫 [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport)來建立完成埠。 此完成埠控制碼可同時用於其他非同步 i/o 作業，以及對等散發的特定作業。

呼叫端應該使用 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數來管理非同步完成。 如果非同步作業失敗， **GetQueuedCompletionStatus** 函式會傳回 **FALSE** ，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回適當的錯誤碼。 如果錯誤碼是 **錯誤 \_ 成功** 以外的任何欄位，則呼叫端應該忽略重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)所有欄位。 如果 **GetQueuedCompletionStatus** 函數傳回 **TRUE**，則非同步作業會成功。

如需詳細資訊，請參閱 [I/o 完成埠](/windows/desktop/FileIO/i-o-completion-ports)。

**以事件為基礎的完成**

如果呼叫端將有效的事件控制碼設定為重迭 [**結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) *hEvent* 欄位，則對等分佈會使用它來表示相關聯的非同步 i/o 作業已完成。

執行緒呼叫端可以在其中一個等候函式中指定重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 手動重設事件物件的控制碼，以管理重迭的作業。 在事件發出信號之後，呼叫端必須呼叫 [**PeerGetOverlappedResult**](https://www.bing.com/search?q=**PeerGetOverlappedResult**) **傳入適當的** 重迭結構。 **PeerGetOverlappedResult** 會傳回 **FALSE** ，而且呼叫端必須呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 才能取得錯誤碼。 如果錯誤碼是 **錯誤 \_ 成功** 以外的任何欄位，則呼叫端應該忽略重 **迭結構的** 所有欄位。 如果 **PeerGetOverlappedResult** 函數傳回 **TRUE**，則非同步作業會成功。

如果呼叫端提供完成埠以及事件，則會使用此事件做為完成機制。

**Windows 7：** 使用 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函式，而不是 [**PeerGetOverlappedResult**](https://www.bing.com/search?q=**PeerGetOverlappedResult**)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[對等散發 API 參考](peer-distribution-api-reference.md)
</dt> </dl>

 

