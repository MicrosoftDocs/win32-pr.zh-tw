---
title: 註冊介面
description: " (RPC) 介面註冊遠端程序呼叫。"
ms.assetid: c22e3fa8-98be-461a-b06d-292d3f655ffc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ea9e851e8c9663c8f66d983d3400b1ee398a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182981"
---
# <a name="registering-interfaces"></a>註冊介面

本節提供註冊 RPC 介面之程式的詳細討論。

本節中的資訊會顯示在下列主題中：

-   [介面註冊函式](#interface-registration-functions)
-   [進入點向量](#entry-point-vectors)
-   [管理員 EPVs](#manager-epvs)
-   [註冊介面的單一實作為](#registering-a-single-implementation-of-an-interface)
-   [註冊介面的多個執行](#registering-multiple-implementations-of-an-interface)
-   [叫用管理員常式的規則](#rules-for-invoking-manager-routines)
-   [分派遠端程序呼叫至 Server-Manager 常式](#dispatching-a-remote-procedure-call-to-a-server-manager-routine)
-   [提供您自己的 Object-Inquiry 函數](#supplying-your-own-object-inquiry-function)

## <a name="interface-registration-functions"></a>介面註冊函式

伺服器會藉由呼叫 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) 函式來註冊其介面。 複雜的伺服器程式通常支援一個以上的介面。 伺服器應用程式必須針對每個支援的介面呼叫此函式一次。

此外，伺服器可以支援相同介面的多個版本，每個版本都有自己的介面函式實作為。 如果您的伺服器程式執行這項工作，則必須提供一組進入點。 進入點是管理員常式，可分派介面版本的呼叫。 每個版本的介面都必須有一個進入點。 進入點的群組稱為進入點向量。 如需詳細資訊，請參閱 [進入點向量](#entry-point-vectors)。

除了標準函式 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)之外，RPC 也支援其他介面註冊功能。 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)函式可讓您指定一組註冊旗標，以擴充 **RpcServerRegisterIf** 的功能， (查看 [介面登錄旗標](interface-registration-flags.md)) 、伺服器可接受的並行遠端程序呼叫要求的最大數目，以及傳入資料區塊的大小上限（以位元組為單位）。

RPC 程式庫也包含稱為 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)的函式。 如同 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) 函式，此函式會註冊介面。 您的伺服器程式也可以使用此函式來指定一組註冊旗標 (請參閱 [介面登錄旗標](interface-registration-flags.md)) 、伺服器可接受之並行遠端程序呼叫要求的最大數目，以及安全性回呼函數。

[**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)和 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)函數會設定內部介面登錄表中的值。 此資料表用來將介面 UUID 和物件 Uuid 對應到管理員 EPV。 管理員 EPV 是函式指標的陣列，在 IDL 檔案中指定的介面中，每個函式原型都只會包含一個函式指標。

如需提供多個 EPVs 以提供介面多個介面的詳細資訊，請參閱 [多個介面實現](#registering-multiple-implementations-of-an-interface)。

執行時間程式庫會使用介面登錄表 (透過呼叫函式 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)或 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)) 和物件登錄表 (設定，方法是呼叫函式 [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)) 將介面和物件 uuid 對應至函式指標。

當您想要讓伺服器程式從 RPC 執行時間程式庫登錄移除介面時，請呼叫 [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) 函數。 從登錄中移除介面之後，RPC 執行時間程式庫將不再接受該介面的新呼叫。

## <a name="entry-point-vectors"></a>進入點向量

 (EPV) 的管理員進入點向量是函式指標的陣列，可指向 IDL 檔案中指定的函式的實作為。 陣列中的元素數目對應到 IDL 檔案中指定的函式數目。 RPC 支援多個進入點向量，代表在介面中指定之函式的多個實作為。

MIDL 編譯器會自動產生用於建立管理員 EPVs 的管理員 EPV 資料類型。 資料類型的名稱為 * if-name ***\_ SERVER \_ EPV**，其中 *if-name* 指定 IDL 檔案中的介面識別碼。

在假設介面中的每個程式都有相同名稱的管理員常式，並且在 IDL 檔案中指定時，MIDL 編譯器會自動建立並初始化預設的管理員 EPV。

當伺服器提供相同介面的多個執行時，伺服器必須為每個執行建立一個額外的管理員 EPV。 每個 EPV 都必須只包含一個進入點， (IDL 檔案中定義之每個程式的函式) 位址。 伺服器應用程式會針對介面的每個額外執行，宣告並 *初始化類型為的 \_ 一個 \_* 管理員 EPV 變數。 為了註冊 EPVs，它會針對每個支援的物件類型呼叫 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)或 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) 一次。

當用戶端對伺服器進行遠端程序呼叫時，會根據介面 UUID 和物件類型，選取包含函式指標的 EPV。 物件類型是由物件 UUID 衍生自物件（object）函數或由 [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)控制的資料表驅動對應。

## <a name="manager-epvs"></a>管理員 EPVs

根據預設，MIDL 編譯器會使用介面 IDL 檔案中的程式名稱來產生管理員 EPV，而編譯器會直接放入伺服器 stub 中。 此預設 EPV 會使用在介面定義中宣告的程式名稱，以靜態方式初始化。

若要使用預設 EPV 註冊管理員，請在對 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)或 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)函數的呼叫中，將 **Null** 指定為 *MgrEpv* 參數的值。 如果管理員所使用的常式名稱對應至介面定義的名稱，您可以使用 MIDL 編譯器所產生之介面的預設 EPV 來註冊這個管理員。 您也可以使用伺服器應用程式提供的 EPV 來註冊管理員。

伺服器可以 (，有時候必須) 建立和註冊介面的非 **null** 管理員 EPV。 若要選取伺服器應用程式提供的 EPV，請將其值已由伺服器宣告的 EPV 位址，傳遞為參數的 *MgrEpv* 值。 *MgrEpv* 參數的非 **null** 值一律會覆寫伺服器 STUB 中的預設 EPV。

MIDL 編譯器會自動產生管理員 EPV 資料類型 (RPC \_ MGR \_ EPV) ，以便讓伺服器應用程式用於建立管理員 EPVs。 針對 IDL 檔案中定義的每個程式，管理員 EPV 必須只包含一個進入點 (函數位址) 。

在下列情況下，伺服器必須提供非 **null** 的 EPV：

-   當管理員常式的名稱與在介面定義中宣告的程式名稱不同時
-   當伺服器使用預設 EPV 來註冊另一個介面的執行時

伺服器會宣告管理員 EPV，方法是在每次執行介面時，初始化類型為的變數（ *如果-name * * * \_ server \_ EPV *）*。

## <a name="registering-a-single-implementation-of-an-interface"></a>註冊介面的單一實作為

當伺服器只提供一個介面的執行時，伺服器只會呼叫 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)或 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) 一次。 在標準案例中，伺服器會使用預設的管理員 EPV。  (例外狀況是當管理員使用的常式名稱與介面中宣告的不同。 ) 

在標準案例中，您可以針對 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)或 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)的呼叫提供下列值：

-   管理員 EPVs

    若要使用預設 EPV，請為 *MgrEpv* 參數指定 **null** 值。

-   管理員類型 UUID

    使用預設 EPV 時，請提供 **null** 值或 *MgrTypeUuid* 參數的 nil UUID，以 nil 管理員類型 UUID 註冊介面。 在此情況下，所有遠端程序呼叫（不論其系結控制碼中的物件 UUID 為何）都會分派至預設 EPV （假設未進行任何 [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) 呼叫）。

    您也可以提供非 nil 管理員類型 UUID。 在此情況下，您也必須呼叫 [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) 常式。

## <a name="registering-multiple-implementations-of-an-interface"></a>註冊介面的多個執行

您可以為 IDL 檔案中指定的 () ，提供一個以上的遠端程式執行。 伺服器應用程式會呼叫 [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) ，將物件 uuid 對應至類型 uuid，並呼叫 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)或 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) ，以將 manager EPVs 與類型 uuid 產生關聯。 當遠端程序呼叫以其物件 UUID 抵達時，RPC 伺服器執行時間程式庫會將物件 UUID 對應至類型 UUID。 然後，伺服器應用程式會使用類型 UUID 和介面 UUID 來選取管理員 EPV。

您也可以指定自己的函式，將物件 UUID 的對應解析為管理員類型 UUID。 當您呼叫 [**RpcObjectSetInqFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsetinqfn)時，可以指定對應函式。

若要提供介面的多個介面，伺服器必須個別呼叫 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) 或 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) 來註冊每個執行。 針對伺服器所註冊的每個執行，它會提供相同的 *IfSpec* 參數，但會提供一組不同的 *MgrTypeUuid* 和 *MgrEpv* 參數。

如果是多個管理員，請使用 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) 或 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) ，如下所示：

-   管理員 EPVs

    若要提供介面的多個介面，伺服器必須：

    -   為每個額外的執行建立非 **null** 的管理員 EPV。
    -   在 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)或 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)中，為 *MgrEpv* 的參數指定非 **null** 的值。

    請注意，伺服器也可以使用預設的管理員 EPV 進行註冊。

-   管理員類型 UUID

    為介面的每個 EPV 提供管理員類型 UUID。 您可以針對 MgrTypeUuid 的其中一個管理員 EPVs，指定 nil 類型 UUID (或 **null** 值) 參數。 每個類型的 UUID 都必須不同。

## <a name="rules-for-invoking-manager-routines"></a>叫用管理員常式的規則

RPC 執行時間程式庫會將傳入的遠端程序呼叫分派給提供所要求 RPC 介面的管理員。 針對某個介面註冊多個管理員時，RPC 執行時間程式庫必須選取其中一個。 為了選取管理員，RPC 執行時間程式庫會使用呼叫的系結控制碼所指定的物件 UUID。

在解讀遠端程序呼叫的物件 UUID 時，執行時間程式庫會套用下列規則：

-   Nil 物件 Uuid

    Nil 物件 UUID 會自動指派給 nil 類型 UUID (不合法，無法在 [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) 常式) 中指定 NIL 物件 uuid。 因此，其系結控制碼包含 nil 物件 UUID 的遠端程序呼叫會自動分派給以 nil 類型 UUID 註冊的管理員（如果有的話）。

-   非 nil 物件 Uuid

    在主體中，其系結控制碼包含非 nil 物件 UUID 的遠端程序呼叫，應該由其類型 UUID 符合物件 UUID 類型的管理員來處理。 不過，識別正確的管理員需要伺服器透過呼叫 [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) 常式來指定該物件 UUID 的型別。

    如果伺服器無法呼叫非 nil 物件 UUID 的 [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) 常式，該物件 uuid 的遠端程序呼叫將會移至服務遠端程序呼叫具有 NIL 物件 uuid 的管理員 EPV， (也就是 NIL 類型 uuid) 。

    如果伺服器指派了非 nil 物件 uuid 的類型 UUID （藉由呼叫 [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) 常式來 UUID 類型 uuid），但尚未藉由呼叫 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) 或 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)來註冊該類型 uuid 的管理員 EPV，就無法執行在系結控制碼中具有非 nil 物件 uuid 的遠端程序呼叫。

下表摘要說明執行時間程式庫用來選取管理員常式的動作。



| 呼叫的物件 UUID | 物件 UUID 的伺服器組類型？ | 伺服器已註冊的 EPV 類型？ | 分派動作                                                                                                                                 |
|---------------------|----------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 零                 | 不適用                   | 是                         | 使用具有 nil 類型 UUID 的管理員。                                                                                                           |
| 零                 | 不適用                   | 否                          | 錯誤 (RPC \_ S \_ 不支援 \_ 的類型) ; 拒絕遠端程序呼叫。                                                                              |
| 非 nil             | 是                              | 是                         | 使用具有相同類型 UUID 的管理員。                                                                                                          |
| 非 nil             | 否                               | 忽略                     | 使用具有 nil 類型 UUID 的管理員。 如果沒有具有 nil 類型 UUID 的管理員，錯誤 (RPC \_ S \_ UNSUPPORTEDTYPE) ; 會拒絕遠端程序呼叫。 |
| 非 nil             | 是                              | 否                          |  (RPC \_ S \_ UNSUPPORTEDTYPE) 時發生錯誤; 拒絕遠端程序呼叫。                                                                                |



 

呼叫的物件 UUID 是在遠端程序呼叫的系結控制碼中找到的物件 UUID。

伺服器會藉由呼叫 [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) 來指定物件的類型 uuid，藉以設定物件 uuid 的型別。

伺服器會使用相同的類型 UUID 來呼叫 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) 或 [**RPCSERVERREGISTERIF2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) ，以註冊管理員 EPV 的類型。

> [!Note]  
> Nil 物件 UUID 一律會自動指派 nil 類型 UUID。 在 [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) 常式中指定 NIL 物件 UUID 是不合法的。

 

## <a name="dispatching-a-remote-procedure-call-to-a-server-manager-routine"></a>分派遠端程序呼叫至伺服器管理員常式

下表顯示 RPC 執行時間程式庫將遠端程序呼叫分派至伺服器管理員常式所需的步驟。

下表說明伺服器註冊預設管理者 EPV 的簡單案例。

**介面登錄表**



| 介面 UUID | 管理員類型 UUID | 進入點向量 |
|----------------|-------------------|--------------------|
| *uuid1*        | 零               | 預設 EPV        |



 

**物件登錄資料表**



| 物件 UUID             | 物件型別 |
|-------------------------|-------------|
| 零                     | 零         |
|  (任何其他物件 UUID)  | 零         |



 

**將系結控制碼對應至進入點向量 (EPV)**



| 從用戶端系結控制碼 (介面 UUID)  | 從用戶端系結控制碼 (的物件 UUID)  | 從物件登錄表 (的物件類型)  | 來自介面登錄表的管理員 EPV ()  |
|---------------------------------------------|------------------------------------------|------------------------------------------|---------------------------------------------|
| *uuid1*                                     | 零                                      | 零                                      | 預設 EPV                                 |
| 同上                               | *uuidA*                                  | 零                                      | 預設 EPV                                 |



 

下列步驟描述當具有介面 UUID 的用戶端呼叫 *uuid1* 時，RPC 伺服器執行時間程式庫所執行的動作（如上表所示）。

1.  伺服器會呼叫 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)或 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) ，將它所提供的介面與 nil 管理員類型 UUID 和 MIDL 產生的預設管理者 EPV 相關聯。 此呼叫會在介面登錄表中新增專案。 介面 UUID 包含在 *IfSpec* 參數中。
2.  依預設，物件登錄表會將所有物件 Uuid 與 nil 類型 UUID 產生關聯。 在此範例中，伺服器不會呼叫 [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)。
3.  伺服器執行時間程式庫會接收遠端程式程式碼，其中包含呼叫所屬的介面 UUID，以及來自呼叫系結控制碼的物件 UUID。

    如需如何將物件 UUID 設定為系結控制碼的討論，請參閱下列函式參考專案：

    -   [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
    -   [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
    -   [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
    -   [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

4.  使用遠端程序呼叫中的介面 UUID 時，伺服器的執行時間程式庫會在介面登錄表中尋找該介面 UUID。

    如果伺服器未使用 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)或 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)註冊介面，則遠端程序呼叫會傳回至呼叫端，且 \_ \_ 如果狀態碼為 UNKNOWN，則會傳回給呼叫端 \_ 。

5.  從系結控制碼使用物件 UUID 時，伺服器的執行時間程式庫會在物件登錄表中找出該物件 UUID。 在此範例中，所有物件 Uuid 都會對應到 nil 物件類型。
6.  伺服器的執行時間程式庫會在介面登錄表中找出「nil 管理員」類型。
7.  將介面登錄表中的介面 UUID 和 nil 類型合併，會解析為預設 EPV，其中包含要針對遠端程序呼叫中找到的介面 UUID 執行的伺服器管理員常式。

假設伺服器會為每個介面提供多個介面和多個執行，如下表所述。

**介面登錄表**



| 介面 UUID | 管理員類型 UUID | 進入點向量 |
|----------------|-------------------|--------------------|
| *uuid1*        | 零               | *epv1*             |
| *uuid1*        | *uuid3*           | *epv4*             |
| *uuid2*        | *uuid4*           | *epv2*             |
| *uuid2*        | *uuid7*           | *epv3*             |



 

**物件登錄資料表**



| 物件 UUID      | 物件型別 |
|------------------|-------------|
| *uuidA*          | *uuid3*     |
| *uuidB*          | *uuid7*     |
| *uuidC*          | *uuid7*     |
| *uuidD*          | *uuid3*     |
| *uuidE*          | *uuid3*     |
| *uuidF*          | *uuid8*     |
| 零              | 零         |
|  (任何其他 UUID)  | 零         |



 

**將系結控制碼對應至進入點向量**



| 從用戶端系結控制碼 (介面 UUID)  | 從用戶端系結控制碼 (的物件 UUID)  | 從物件登錄表 (的物件類型)  | 來自介面登錄表的管理員 EPV ()  |
|---------------------------------------------|------------------------------------------|------------------------------------------|---------------------------------------------|
| *uuid1*                                     | 零                                      | 零                                      | *epv1*                                      |
| *uuid1*                                     | *uuidA*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid1*                                     | *uuidD*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid1*                                     | *uuidE*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid2*                                     | *uuidB*                                  | *uuid7*                                  | *epv3*                                      |
| *uuid2*                                     | *uuidC*                                  | *uuid7*                                  | *epv3*                                      |



 

下列步驟描述伺服器執行時間程式庫所採取的動作，如上表所示，當具有介面 UUID *uuid2* 和物件 uuid *uuidC* 的用戶端呼叫它時。

1.  伺服器會呼叫 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)或 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) ，將它所提供的介面與不同的管理員 EPVs 產生關聯。 介面登錄表中的專案會反映 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)或 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) 的四個呼叫，以提供兩個介面，並針對每個介面 (EPVs) 。
2.  伺服器會呼叫 [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) 來建立它所提供之每個物件的型別。 除了 nil 物件與 nil 型別的預設關聯以外，在物件登錄表中未明確找到的所有其他物件 Uuid 也會對應到 nil 類型 UUID。

    在此範例中，伺服器會呼叫 [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) 常式六次。

3.  伺服器執行時間程式庫會接收遠端程序呼叫，其中包含呼叫所屬的介面 UUID，以及來自呼叫系結控制碼的物件 UUID。
4.  使用遠端程序呼叫中的介面 UUID，伺服器的執行時間程式庫會找出介面登錄表中的介面 UUID。
5.  從系結控制碼使用 *uuidC* 物件 uuid 時，伺服器的執行時間程式庫會在物件登錄表中找出物件 uuid，併發現它會對應到類型 *uuid7*。
6.  為了找出管理員類型，伺服器的執行時間程式庫會合並介面登錄表中的介面 UUID、 *uuid2* 和類型 *uuid7* 。 這會解析為 *epv3*，其中包含要針對遠端程序呼叫執行的伺服器管理員常式。

*Epv2* 中的常式永遠不會執行，因為伺服器尚未呼叫 [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)常式，以將類型 UUID 為 *uuid4* 的任何物件加入至物件登錄表。

具有介面 UUID *uuid2* 和物件 UUID *uuidF* 的遠端程序呼叫會傳回具有 RPC \_ \_ 未知 \_ MGR 類型狀態碼的呼叫端 \_ ，因為伺服器未呼叫 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)、 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)或 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) 來註冊管理員類型 *uuid8* 的介面。

## <a name="return-values"></a>傳回值

此函數會傳回下列其中一個值。



| 值                             | 意義                      |
|-----------------------------------|------------------------------|
| RPC \_ S \_ 確定                        | Success                      |
| \_ \_ \_ 已註冊 RPC S \_ 類型 | 類型 UUID 已經註冊 |



 

## <a name="supplying-your-own-object-inquiry-function"></a>提供您自己的物件查詢函式

請考慮管理許多不同類型之物件的伺服器。 當伺服器啟動時，伺服器應用程式必須針對每個物件呼叫函式 [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) ，即使用戶端可能只參考其中幾個物件 (或花很長的時間來參考它們) 。 這上千個物件可能會在磁片上，因此抓取其類型會相當耗時。 此外，將物件 UUID 對應到管理員類型 UUID 的內部資料表基本上會複製與物件本身維護的對應。

為了方便起見，RPC 函數集包含函式 [**RpcObjectSetInqFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsetinqfn)。 使用此函式，您可以提供自己的物件查詢函式。

例如，您可以在將物件100–199對應至類型1、200–299至類型第2個時，提供您自己的物件查詢函式，依此類推。 物件查詢函式也可以延伸至分散式檔案系統，其中伺服器應用程式沒有 (物件 Uuid) 可用的所有檔案清單，或檔案系統中的物件 Uuid 名稱檔案，而且您不想預先載入物件 Uuid 和類型 Uuid 之間的所有對應。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
</dt> <dt>

[**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)
</dt> <dt>

[**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)
</dt> <dt>

[**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 




