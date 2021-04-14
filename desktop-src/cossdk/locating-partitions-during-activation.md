---
description: 在啟用期間尋找磁碟分割
ms.assetid: a5452ed6-ab0f-4d38-bc16-1de6cbf57486
title: 在啟用期間尋找磁碟分割
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e8912c8277d79c1a20300a1a880644801d0bcb
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104555711"
---
# <a name="locating-partitions-during-activation"></a>在啟用期間尋找磁碟分割

找出要啟用元件的正確磁碟分割取決於下列各項：

-   呼叫程式中用來啟動元件的函式呼叫和參數
-   要啟用的元件是本機或遠端
-   資料分割快取的內部使用

## <a name="the-calling-program"></a>呼叫程式

COM + 會根據呼叫程式啟動元件的方式，選取要啟用的資料分割。

有三種不同的動作，可讓 COM + 在選取用於元件啟用的資料分割時採用。 採取的動作取決於呼叫程式如何將物件具現化，也就是函式呼叫是否包含分割區識別碼和 CLSID 所組成的資料分割標記，或是只包含 CLSID。

下表顯示 COM + 可採用的各種動作（依優先順序）以找出資料分割。



| 函式呼叫                                                  | 參數                                                      | COM + 動作                                                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) 或 **GetObject**<br/> | 分割區標記 (包括資料分割識別碼和 CLSID) <br/> | 使用資料分割標記中指定的分割區識別碼。<br/>                                                                                                                           |
| [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)<br/>        | CLSID<br/>                                               | 使用使用者識別之預設分割區的分割區識別碼，或在相同進程中先前元件啟用期間新增至內容的資料分割識別碼。<br/> |



 

下列各節將說明上表所列的 COM + 動作。

## <a name="use-of-partition-monikers"></a>使用分割區的名字

您可以使用資料 *分割標記*，在函式呼叫內明確選取資料分割。 在程式碼中，會使用資料分割標記來明確指定已啟動元件的資料分割。 如果使用資料分割標記來找出分割區，則會從該分割區進行啟用。 也就是說，在標記中包含的資料分割識別碼會優先于使用者的預設分割區，或是存在於呼叫端內容中的資料分割識別碼。

在 c + + 程式碼中，使用資料分割標記的語法如下所示：


```C++
HRESULT CoGetObject(
  L"partition:partitionGUID/new:clsid",
  pBindOptions,
  IID_IUnknown,
  (void**)&pIUnknown);
```



下列範例顯示 c + + 程式碼的程式碼片段，其中會使用分割區的標記做為 [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) 函數的引數：


```C++
// Create CLSID1 configured in the Production partition.
HRESULT hr = CoGetObject(
  L"partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1",
  pBindOptions, IID_IUnknown, (void**)&pIUnknown);
```



在 Visual Basic 程式碼中，資料分割標記的語法如下所示：


```VB
GetObject("partition:partitionGUID/new:CLSID") As Object
```



下列範例會顯示 Visual Basic 程式碼的程式碼片段，其中資料分割標記會當做 **GetObject** 函數的引數使用：


```VB
Dim objCLSID1 As Object
Set objCLSID1 = GetObject( _
   "partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1")
```



## <a name="use-of-default-mapping"></a>使用預設對應

當 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數用來啟動元件時，使用元件的 CLSID 時，com + 會使用預設的使用者識別對應，也就是使用者在 Active Directory 內對應的資料分割集。 但是，如果使用者未對應到 Active Directory 內的資料分割集，則會選取全域資料分割。

## <a name="use-of-partition-ids-and-object-context"></a>使用資料分割識別碼和物件內容

指派給新分割區的五個屬性之一是分割區識別碼。 當用戶端程式呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數來具現化物件時，會將資料分割識別碼加入至內容。 使用來自內容的資料分割識別碼來找出分割區是很重要的，因為它可確保在開始執行鏈之後，資料分割識別碼會維持不變，除非它透過分割區標記明確變更。

如需在啟用期間尋找資料分割的詳細資訊，請參閱 [Com + 佇列元件和](com--queued-components-and-partitions.md)分割區。

## <a name="local-and-remote-activation"></a>本機和遠端啟用

-   如果所呼叫的元件存在於另一部電腦上，磁碟分割屬性 (包括分割區識別碼) 會封送處理至另一部電腦，而且該元件會從已封送處理的分割區啟用。 如果未封送處理資料分割識別碼，COM + 會使用對應至 Active Directory 內使用者識別的預設資料分割集。

## <a name="the-partition-cache"></a>分割區快取

在網域環境中，COM + 會使用 Active Directory 中的對應，找出正確的資料分割以進行元件啟用。 不過，在 Active Directory 中頻繁地查閱可能會導致網路流量過高。 為了將在 Active Directory 中頻繁查閱使用者對分割集對應所產生的網路流量降至最低，COM + 會使用 *分割* 區快取。

分割區快取包含在使用者身分識別或 Ou 與其分割集之間的 Active Directory 中進行的對應。 此分割區快取位於 COM + 應用程式所在的應用程式伺服器上。

當 COM + 需要判斷使用者的預設分割區，或驗證使用者對資料分割的存取權限時，它會在本機檢查資料分割快取以查詢使用者的對應，而不是從遠端檢查 Active Directory。

如果分割區快取中的查閱失敗，COM + 就會檢查 Active Directory。 如果 Active Directory 中的查閱成功，COM + 會將該對應儲存在分割區快取中。 下次對該使用者對分割區對應進行查閱時，COM + 會在分割區快取中找到它。

下圖顯示 COM + 用來尋找元件啟用之分割區的進程。

![此圖顯示 COM + 用來尋找元件啟用之分割區之進程的疑難排解樹狀結構。](images/5d00eb4e-4572-491c-85e9-33ceed2cd753.png)

快取的大小和快取專案的到期時間是透過登錄機碼設定。 如需設定這些登錄機碼的詳細資訊，請參閱 [建立和設定 COM +](creating-and-configuring-com--partitions.md)分割。

> [!Note]  
> 如果伺服器電腦與網路中斷連線，而伺服器中斷連線時，使用者對分割區的對應會變更，則磁碟分割快取可能會包含過期的使用者對分割區對應。 如果使用者對分割區對應是用來啟動元件的機制，這可能會導致啟用錯誤。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[找出要啟用的元件](locating-a-component-for-activation.md)
</dt> </dl>

 

