---
title: COM 技術總覽
ms.assetid: 519c87cc-b442-4187-af2a-124a1e4e8b49
description: 深入瞭解： COM 技術總覽
keywords:
- COM 技術總覽 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 851a2147c1bbe31dd8c212f7f23089c522cf7998bc2d336e95120277fba84275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854758"
---
# <a name="com-technical-overview"></a>COM 技術總覽

本主題提供 Microsoft 元件物件模型 (COM) 的總覽：

-   [COM 簡介](#introduction-to-com)
-   [物件和介面](#objects-and-interfaces)
-   [介面執行](#interface-implementation)
-   [IUnknown 介面](#the-iunknown-interface)
-   [用戶端/伺服器模型](#the-clientserver-model)
-   [服務控制管理員](#service-control-manager)
-   [可 重用](#reusability)
-   [儲存體和資料流程物件](#storage-and-stream-objects)
-   [資料轉送](#data-transfer)
-   [遠端](#remoting)
-   [安全性](#security)
-   [相關主題](#related-topics)

## <a name="introduction-to-com"></a>COM 簡介

Microsoft 元件物件模型 (COM) 會定義二進位互通性標準，以建立在執行時間進行互動的可重複使用軟體程式庫。 您可以使用 COM 程式庫，而不需要將它們編譯到應用程式中。 COM 是許多 Microsoft 產品和技術的基礎，例如 Windows Media Player 和 Windows Server。

COM 定義適用于許多作業系統和硬體平臺的二進位標準。 針對網路運算，COM 會定義標準電傳格式和通訊協定，以便在不同硬體平臺上執行的物件之間進行互動。 COM 與實語言無關，這表示您可以使用不同的程式設計語言（例如 c + + 和 .NET Framework 中的語言）來建立 COM 程式庫。

COM 規格提供可讓您重複使用跨平臺軟體的所有基本概念：

-   元件之間函式呼叫的二進位標準。
-   將函數的強型別分組布建至介面。
-   提供多型、功能探索和物件存留期追蹤的基底介面。
-   可唯一識別元件及其介面的機制。
-   從部署建立元件實例的元件載入器。

COM 有許多部分可一起運作，以建立從可重複使用的元件建立的應用程式：

-   提供符合 COM 規格之執行時間環境的 *主機系統* 。
-   定義功能合約的 *介面*，以及用來執行介面的 *元件*。
-   提供元件給系統的 *伺服器*，以及使用元件所提供功能的 *用戶端*。
-   追蹤元件部署在本機和遠端主機 *上的登錄* 。
-   *服務控制管理員*，可在本機和遠端主機上尋找元件，並將伺服器連接至用戶端。
-   *結構化儲存體* 通訊協定，定義如何流覽主機檔案系統上的檔案內容。

跨主機和平臺啟用程式碼重複使用是 COM 的核心。 可重複使用的介面實名為 *元件*、 *元件物件* 或 *COM 物件*。 元件會執行一個或多個 COM 介面。

您可以藉由設計程式庫所實行的介面來定義自訂 COM 程式庫。 您程式庫的取用者可以探索及使用其功能，而不需要瞭解您的程式庫部署和實行詳細資料。

## <a name="objects-and-interfaces"></a>物件和介面

COM 物件會透過 *介面*（成員函式的集合）來公開其功能。 COM 介面會定義元件的預期行為和責任，並且會指定提供一小段相關作業的強型別合約。 COM 元件之間的所有通訊都是透過介面進行，而元件所提供的所有服務都是透過其介面公開。 呼叫端只能存取介面成員函式。 除非在介面中公開，否則呼叫端無法使用內部狀態。

介面是強型別。 每個介面都有自己的唯一介面識別碼，名稱為 IID，以消除人們可讀取的名稱可能發生的衝突。 IID 是 (GUID) 的全域唯一識別碼，這與 Open Software Foundation (憑證) 分散式運算環境 () 中所定義的通用唯一識別碼 (UUID) 相同。 當您建立新的介面時，您必須為該介面建立新的識別碼。 當呼叫端使用介面時，它必須使用唯一識別碼。 這項明確的識別會藉由消除會導致運行時失敗的命名衝突，來改善穩定性。

當您定義新的介面時，可以使用 (IDL) 的介面定義語言來建立介面定義。 從這個介面定義中，Microsoft IDL 編譯器會產生使用介面的應用程式所使用的標頭檔，以及用來處理遠端程序呼叫的原始程式碼。 由 Microsoft 提供的 IDL 是以 DCE IDL 的簡單延伸模組為基礎，這是遠端程序呼叫的業界標準， (RPC) 為基礎的分散式運算。 IDL 是可方便使用介面設計師的工具，而且不是 COM 互通性的核心。 使用 IDL 時，您不需要針對每個程式設計環境手動建立標頭檔。 如需詳細資訊，請參閱 [定義 COM 介面](defining-com-interfaces.md)。

COM 介面會謹慎使用繼承。 COM 僅支援介面繼承，以重複使用與基底介面相關聯的合約。 COM 不支援選擇性繼承;因此，如果某個介面繼承自另一個介面，它會包含基底介面定義的所有函式。 此外，介面只會使用單一繼承（而不是多個繼承）來取得基底介面的函式。

## <a name="interface-implementation"></a>介面執行

您無法自行建立 COM 介面的實例。 相反地，您會建立可執行介面之類別的實例。 在 c + + 中，COM 介面會模型化為 *抽象基類*，這表示介面是僅包含單純虛擬成員函式的 c + + 類別。 C + + 程式庫會藉由繼承一或多個介面的成員函式簽章、覆寫每個成員函式，以及為每個函式提供執行，來執行 COM 物件。

您可以使用任何支援函式指標概念的程式設計語言來執行 COM 介面。 例如，在 C 中，介面是包含函式指標資料表指標的結構，介面中的每個方法都有一個指標。

當您執行介面時，您的類別必須為介面中的每個函式提供實作為。 如果類別沒有任何要在介面函式中執行的工作，則實作為單一 return 語句。

COM 類別的識別方式是使用唯一的128位類別識別碼 (CLSID) ，其會將類別與檔案系統中的特定部署產生關聯，而 Windows 是 DLL 或 EXE。 CLSID 是 GUID，這表示沒有其他類別具有相同的 CLSID。 使用唯一類別識別碼可避免類別之間的名稱衝突。 例如，兩個不同的廠商可以撰寫名為 CStack 的類別，但是這兩個類別都有唯一的 CLSID，因此可以避免任何可能發生衝突的情況。

您可以使用 [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)函式或使用 COM 撰寫工具（例如 Visual Studio）來取得新的 CLSID，此工具會在內部呼叫此函式。

## <a name="the-iunknown-interface"></a>IUnknown 介面

所有 COM 介面都會繼承自 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面。 **IUnknown** 介面包含多型和實例存留期管理的基本 COM 作業。 **IUnknown** 介面有三個成員函式，名為 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))、 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)和 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)。 所有 COM 物件都必須執行 **IUnknown** 介面。

[**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))成員函式提供 COM 的多型。 呼叫 **QueryInterface** ，在執行時間判斷 COM 物件是否支援特定介面。 如果 COM 物件會執行所 `ppvObject` 要求的介面，則會傳回參數中的介面指標，否則會傳回 `NULL` 。 **QueryInterface** 成員函式可讓您在 COM 物件支援的所有介面之間進行導覽。

COM 物件實例的存留期是由其 *參考計數* 所控制。 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)成員函式 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)和 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)控制計數。 **AddRef** 會遞增計數， **並將** 計數遞減。 當參考計數到達零時， **釋放** 成員函式可能會釋放實例，因為沒有任何呼叫端正在使用它。

## <a name="the-clientserver-model"></a>用戶端/伺服器模型

COM 類別會執行多個 COM 介面。 此實作為由呼叫端與 COM 類別的實例互動時所執行的二進位檔。 COM 可在不同的應用程式中使用類別，包括在不知道特定類別的情況下撰寫的應用程式。 在 Windows 平臺上，類別會存在於動態連結的程式庫 (DLL) 或 (EXE) 的另一個應用程式中。

在其主機系統上，COM 會針對安裝在系統上的 COM 物件，維護所有 Clsid 的註冊資料庫。 註冊資料庫是每個 CLSID 和裝載對應類別之 DLL 或 EXE 的位置之間的對應。 每當呼叫端想要建立 COM 類別的實例時，COM 就會查詢這個資料庫。 呼叫端必須知道 CLSID 才能要求類別的新實例。

COM 物件與其呼叫端之間的互動會模型化為用戶端/伺服器關聯性。 用戶端是從系統要求 COM 物件的呼叫端，而伺服器是裝載提供服務給用戶端之 COM 物件的模組。

COM 用戶端是任何將 CLSID 傳遞給系統以要求 COM 物件實例的呼叫端。 建立實例的最簡單方式是呼叫 COM 函式 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)。

[**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)函式會建立指定之 CLSID 的一個實例，並傳回用戶端所要求之型別的介面指標。 用戶端會負責管理實例的存留期，方法是在用戶端完成使用它時呼叫它的 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 函數。 若要根據單一 CLSID 建立多個物件，請呼叫 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) 函數。 若要連接到已經建立並執行的物件，請呼叫 [**GetActiveObject**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-getactiveobject) 函數。

COM 伺服器提供系統的 COM 執行。 伺服器會將 CLSID 與 COM 類別產生關聯、裝載類別的實作為來建立類別的實例，並提供用於卸載伺服器的類別 factory。

> [!Note]  
> COM 伺服器與提供給系統的 COM 物件不同。

 

若要啟用 COM 物件的建立，COM 伺服器必須提供 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 介面的實作為。 用戶端可以呼叫 [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) 方法來要求 COM 物件的新實例，但這類要求通常會封裝在 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數中。

您可以將 COM 伺服器部署為共用程式庫，該程式庫會在執行時間載入至用戶端的進程中 Windows 平臺上的 (DLL) 或作為 Windows 平臺) 上的可執行模組 (EXE。 如需詳細資訊，請參閱 [註冊 COM 應用程式](registering-com-applications.md)。

## <a name="service-control-manager"></a>服務控制管理員

服務控制管理員 (SCM) 處理 COM 物件實例的用戶端要求。 下列清單顯示事件的順序：

-   用戶端會藉由呼叫函式（例如 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 和 com 物件的 CLSID），向 Com 程式庫要求 com 物件的介面指標。
-   COM 程式庫會查詢 SCM，以找出對應于所要求 CLSID 的伺服器。
-   SCM 會尋找伺服器，並要求從伺服器所提供的 class factory 建立 COM 物件。
-   如果成功，COM 程式庫會將介面指標傳回給用戶端。

在 COM 系統將伺服器物件連接至用戶端之後，用戶端和物件會直接進行通訊。 透過中繼執行時間呼叫不會增加額外負荷。

當您向主機系統註冊 COM 伺服器時，可以指定不同的伺服器啟動方式。 下列清單顯示 SCM 可以啟用 COM 伺服器的三種方式：

-   同進程： SCM 會傳回包含物件服務器執行之 DLL 的檔案路徑。 COM 程式庫會載入 DLL，並針對其 class factory 介面指標進行查詢。
-   Local： SCM 啟動可在啟動時註冊 class factory 的本機可執行檔，且其介面指標可供系統和用戶端使用。
-   Remote：本機 SCM 從遠端電腦上執行的 SCM 取得 class factory 介面指標。

當用戶端要求 COM 物件時，COM 程式庫會聯繫本機主機上的 SCM。 SCM 會找出適當的 COM 伺服器（可能是本機或遠端），而伺服器會將介面指標傳回伺服器的 class factory。 當 class factory 可供使用時，COM 程式庫或用戶端可以使用 class factory 來建立要求的物件。 如需詳細資訊，請參閱 [執行 IClassFactory](implementing-iclassfactory.md)。

## <a name="reusability"></a>重複使用性

COM 支援 *黑箱* 重複使用性，這表示可重複使用元件的執行詳細資料不會公開給用戶端。 為了達到黑箱重複使用性，COM 支援兩種機制，其中一個物件可以重複使用另一個物件。 這兩種重複使用 *形式稱為內含專案和**匯總*。 依照慣例，所要使用的物件會命名為 *內建物件*，而使用內建物件的物件會命名為 *外部物件*。

在內含專案中，外部物件的行為是內建物件的用戶端。 外部物件是內建物件的邏輯容器，當外部物件使用內建物件的服務時，外部物件會將執行委派給內建物件的介面。 這表示外部物件會根據內建物件的服務來執行。 外部物件可能不支援與內建物件相同的介面，而且外部物件可能會使用內建物件的介面，以協助在外部物件上執行不同介面的元件。

在匯總中，外部物件會公開內建物件的介面，就如同它們是在外部物件上執行一樣。 當外部物件一律會將其中一個介面的每個呼叫委派給內建物件的相同介面時，這會很有用。 匯總是方便的，可讓外部物件避免額外的執行負擔。

如需詳細資訊，請參閱 [重複使用物件](reusing-objects.md)。

## <a name="storage-and-stream-objects"></a>儲存體和資料流程物件

COM 物件會使用 *結構化儲存區* 將狀態儲存至檔案，這是一種持續性儲存格式，可讓您使用檔案系統語義來流覽檔案的內容。 以這種方式來處理檔案的內容，可以在進程之間提供累加式存取、交易和共用等功能。

COM 持續性儲存體規格提供兩種類型的儲存體元素：儲存物件和資料流程物件。 這些物件是由 COM 程式庫所執行，而且使用者應用程式很少會執行這些儲存元素。 儲存體物件會執行 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage)介面，而資料流程物件則會執行 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面。

資料流程物件包含資料，而且在概念上類似于檔案系統中的單一檔案。 每個串流都具有存取權限和單一搜尋指標。 透過 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) 介面，您可以讀取、寫入、搜尋和執行資料流程基礎資料的其他作業。 資料流程的命名方式是使用文字字串。 它可以包含任何內部結構，因為這是一般的位元組資料流程。 此外， **IStream** 介面中的函式類似于標準檔案處理型函式，例如 ANSI C 執行時間程式庫中的函數。

儲存物件在概念上類似于檔案系統中的目錄。 每個儲存體可包含任意數目的子儲存體物件和任意數量的資料流程。 每個儲存體都有自己的存取權限。 透過 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) 介面，您可以執行像是列舉、移動、複製、重新命名、建立及刪除元素等作業。 儲存物件不會儲存應用程式定義的資料，但會以隱含的方式儲存專案名稱， (儲存和它所包含的資料流程) 。

當程式是根據主機平臺上的 COM 規格來執行時，可以在進程間共用儲存體和資料流程物件。 這可讓執行同進程或跨進程的物件擁有相同的累加式存取權來存取其檔案儲存體。 由於 COM 會個別載入至每個進程，因此它會使用作業系統支援的共用記憶體機制，來傳達開啟專案的狀態及其處理常式之間的存取模式。

結構化檔案中的每個儲存和資料流程物件都有一個名稱來識別它。 名稱是遵循特定慣例的字串。 如需詳細資訊，請參閱[儲存體物件命名慣例](/windows/desktop/Stg/storage-object-naming-conventions)。 名稱會傳遞至 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) 函式，以指定要在儲存體中操作的元素。 根儲存物件的名稱與基礎檔案系統中的檔案名相同，而且這些名稱必須遵循檔案系統的慣例和限制。 傳遞給儲存相關函式的字串，這些函式會將名稱檔案傳遞至檔案系統，而不需要解讀或變更。

包含在儲存物件內的專案名稱，是由有問題的特定儲存物件的實作為管理。 所有儲存體物件的執行都必須支援長度為32個字元的專案名稱，而某些執行可能會支援較長的名稱。 名稱會儲存並保留大小寫，但會比較為不區分大小寫。 定義儲存元素名稱的應用程式必須選擇可在任一情況下運作的名稱。

您可以使用 COM 所執行的函式和介面，來存取結構化儲存體檔案中的每個元素。 這表示其他應用程式可以流覽檔案，方法是以提供類似目錄服務的 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) 介面函式進行流覽。 此外，其他應用程式也可以使用檔案的資料，而不需要執行寫入檔案的應用程式。 當 COM 應用程式存取另一個應用程式的結構化儲存體檔案時，會套用標準 Windows 存取權限，而且應用程式必須有足夠的許可權。

COM 物件可以讀取和寫入持續性儲存區。 用戶端會根據作業的內容，查詢 COM 物件的其中一個持續性相關的介面。 COM 物件可以執行下列介面的任何組合：

-   [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)： COM 物件會讀取其持續性狀態，並將其寫入儲存物件。 用戶端會透過此介面提供具有 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) 指標的物件。 這是唯一的持續性介面，其中包含累加式存取的語法。
-   [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)： COM 物件會讀取其持續性狀態，並將其寫入資料流程物件。 用戶端會透過這個介面提供具有 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) 指標的物件。
-   [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)： COM 物件會將其持續性狀態直接讀取並寫入基礎系統上的檔案中。 此介面不牽涉到 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) 或 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) ，除非基礎檔案是透過這些介面存取，但 **IPersistFile** 介面沒有適用于儲存體和資料流程的語法。 用戶端會提供具有檔案名的物件，並呼叫 [**Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersistfile-save) 或 [**Load**](/windows/desktop/api/ObjIdl/nf-objidl-ipersistfile-load) 函數。

## <a name="data-transfer"></a>資料轉送

結構化儲存體提供 COM 物件與進程之間的資料交換基礎，名為「 *制式資料傳輸*」。 在 OLE 2 中執行 COM 之前，Windows 的資料傳輸是由 *傳輸通訊協定*（例如剪貼簿和拖放通訊協定）所指定。 每個傳輸通訊協定都有自己的一組函式，這些函式會將通訊協定系結至查詢，而且需要特定程式碼來處理每個不同的通訊協定和交換程式。 制式資料傳輸代表使用 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 介面的所有資料傳輸，可將一般資料交換作業與傳輸通訊協定分隔開來。

[**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)介面會針對資料、查詢和列舉，以及當物件中的資料變更時偵測到的通知，封裝標準的 get 和 set 作業。 制式資料傳輸可提供豐富的資料格式描述，以及使用不同的儲存體媒體進行資料傳輸。

在統一的資料傳輸期間，所有通訊協定都會交換指向 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 介面的指標。 伺服器是資料的來源，並會執行一個資料物件，此物件可在任何資料交換通訊協定中使用。 用戶端會在收到來自任何通訊協定的 **IDataObject** 指標時取用資料，並要求資料物件中的資料。 指標交換之後，雙方都會透過 **IDataObject** 介面，以一致的方式處理資料交換。

COM 會定義兩個資料結構，以啟用統一的資料傳輸。 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc)結構代表通用的剪貼簿格式，而 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構則代表傳送媒體作為記憶體控制碼。

用戶端會建立 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 結構來指出它從資料來源要求的資料類型，而且資料來源會使用它來描述它所提供的格式。 用戶端會要求其 [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) 介面，以查詢資料來源的可用格式。 如需詳細資訊，請參閱 [FORMATETC 結構](the-formatetc-structure.md)。

用戶端會建立 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構，並將它傳遞至「未處理 [**」方法，**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) 而資料物件會傳回所提供 **STGMEDIUM** 結構中的資料。

[**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構可讓用戶端和資料來源選擇最有效率的 exchange 媒體。 例如，如果要交換的資料很大，資料來源可以將磁片型媒體表示為其慣用格式，而不是主儲存體。 這種彈性可提供有效率的資料交換，就像傳遞指標給 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) 或 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)一樣快。 如需詳細資訊，請參閱 [STGMEDIUM 結構](the-stgmedium-structure.md)。

資料來源的用戶端可能需要在資料變更時發出通知。 COM 會使用實 [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)介面的 *建議接收* 物件來處理資料變更通知。 建議接收物件和 **IAdviseSink** 介面是由用戶端所執行，該用戶端會將 **IAdviseSink** 指標傳遞至資料來源。 當資料來源偵測到基礎資料變更時，它會呼叫 **IAdviseSink** 方法來通知用戶端。 如需詳細資訊，請參閱 [資料通知](data-notification.md)。

## <a name="remoting"></a>遠端

COM 可啟用遠端和分散式運算。 *介面遠端* 功能可讓成員函式將介面指標傳回至不同進程或不同主機電腦上的 COM 物件。 執行介面遠端的基礎結構對於用戶端和物件服務器都是透明的。 用戶端和伺服器都不需要另一個部署詳細資料，也能透過遠端介面進行通訊。 用戶端會呼叫相同介面上的成員函式，以便與本機主機或遠端電腦上同進程、跨進程的 COM 物件進行通訊。 相同介面上的本機和遠端呼叫與用戶端不區分。

若要與 COM 物件進行通訊，用戶端一律會呼叫同進程執行。 如果 COM 物件是同進程，則呼叫是 direct。 如果 COM 物件是跨進程或遠端，COM 會提供 *proxy* 執行，使用遠端程序呼叫 (RPC) 通訊協定來轉送物件的呼叫。

COM 物件一律會透過同進程執行，從用戶端接收呼叫。 如果呼叫端在同進程中，則呼叫是 direct。 如果呼叫端在進程外或遠端，COM 會提供 *存根* 執行，以接收用戶端進程中 proxy 的遠端程序呼叫。

*封送處理* 是封裝呼叫堆疊以從 proxy 傳輸到 stub 的程式。 *封送* 是在接收端發生的解除封裝。 傳回值會從存根封送處理並取消封送處理至 proxy。 這種通訊也稱為透過 *網路* 傳送通話。

每個不同的資料類型都有封送處理的規則。 介面指標也有封送處理通訊協定，它封裝在 [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) 函式中。 在大部分的情況下， *標準介面封送處理*（由系統提供）已足夠，但 COM 物件可選擇性地執行 *自訂介面封送處理* ，以控制如何建立遠端物件 proxy。 如需詳細資訊，請參閱 [物件間通訊](inter-object-communication.md)。

## <a name="security"></a>安全性

COM 提供兩種形式的應用程式安全性。 其中一個是 *啟用安全性*，可指定新物件的建立方式、用戶端連接至新的和現有物件的方式，以及某些公用服務（例如類別資料表和執行中的物件資料表）的安全方式。 另一個是 *呼叫安全性*，它會指定在用戶端與 COM 物件之間建立的連線時，安全性的運作方式。

「服務控制管理員」會自動套用「啟用安全性」 (SCM) 。 當 SCM 收到取得 COM 物件的要求時，它會根據儲存在登錄中的安全性資訊來檢查要求。

SCM 執行通常會提供登錄導向的設定，以管理部署的類別和主機上的特定使用者帳戶。 如需詳細資訊，請參閱 [啟用安全性](activation-security.md)。

呼叫安全性會自動套用，或由應用程式強制執行。 如果應用程式提供設定資訊，COM 會執行必要的檢查以保護應用程式。

自動機制會檢查進程的安全性，但不會檢查個別物件或方法的安全性。 如果應用程式需要更精細的安全性，COM 會提供應用程式可使用的函式來執行自己的安全性檢查。

自動和自訂機制可以一起使用，因此應用程式可能會要求 COM 執行自動安全性檢查，然後執行它自己的動作。

COM 呼叫安全性服務分為下列類別：

-   用戶端和伺服器所呼叫的一般函式，可讓您初始化自動安全性機制，以及註冊自動驗證服務。 一般呼叫安全性 Api 是 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 和 [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) 函數。
-   用戶端 proxy 上的介面，可讓用戶端控制對個別介面之呼叫的安全性。 [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)介面和 [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket)、 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)和 [**CoCopyProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy)函數會在遠端物件上提供呼叫安全性。
-   伺服器端函式和呼叫內容介面，可讓伺服器取得有關呼叫的安全性資訊，以及模擬呼叫者。 [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity)介面和 [**CoGetCallCoNtext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)、 [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)和 [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)函式提供伺服器端呼叫安全性。

通常，用戶端會查詢 COM 物件以取得 [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) 介面，這個介面是由遠端層在本機執行。 用戶端會使用此介面來控制 COM 物件上個別介面 proxy 的安全性，然後再對其中一個介面進行呼叫。

當呼叫抵達伺服器時，伺服器可能會呼叫 [**CoGetCallCoNtext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) 函式來取出 [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) 介面，如此可讓伺服器檢查用戶端的驗證，並在必要時模擬用戶端。 **IServerSecurity** 物件在呼叫期間有效。

呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 函式來初始化安全性層級，並將指定的值設定為安全性預設值。 如果處理常式未呼叫 **CoInitializeSecurity**，COM 會在第一次將介面封送處理或取消封送處理時自動呼叫它，以註冊系統預設安全性。 **CoInitializeSecurity** 函數可讓用戶端建立進程的預設呼叫安全性，以避免在個別 proxy 上使用 [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) 。 **CoInitializeSecurity** 函式可讓伺服器為進程註冊自動驗證服務。 如需詳細資訊，請參閱 [使用 CoInitializeSecurity 設定 Process-Wide 安全性](setting-processwide-security-with-coinitializesecurity.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 用戶端和伺服器](com-clients-and-servers.md)
</dt> <dt>

[定義 COM 介面](defining-com-interfaces.md)
</dt> <dt>

[註冊 COM 應用程式](registering-com-applications.md)
</dt> <dt>

[COM 中的安全性](security-in-com.md)
</dt> <dt>

[進程、執行緒和單元](processes--threads--and-apartments.md)
</dt> </dl>

 

 
