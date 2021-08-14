---
title: 系結至 Active Directory 物件
description: 系結至 Active Directory 物件最常見的方式，就是在 ADSI 用戶端和 ADSI 提供者之間使用 GetObject 函數。
ms.assetid: d278ea26-2fd5-4343-8d87-ff85515325fb
ms.tgt_platform: multiple
keywords:
- 系結至 Active Directory 物件 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc788ed9eb124e1da6c21848f02393d46608f00dd3a9e779788fa54429922400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429129"
---
# <a name="binding-to-an-active-directory-object"></a>系結至 Active Directory 物件

系結至 Active Directory 物件最常見的方式，就是在 ADSI 用戶端和 ADSI 提供者之間使用 **GetObject** 函數。 這也是顯示提供者元件接收和服務要求方式的最簡單方式。 ADSI API 函數 [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)或 Visual Basic 函式 **GetObject** 都會遵循相同的系結步驟。

在這個範例中，假設 ADSI 用戶端是一個 ADSI 檢視器應用程式，它的使用者介面收到了 ADsPath "Sample://Seattle/Redmond/Shelly" (1) 。 下圖詳細說明按下流程箭號的事件順序。

![adsi 元件的詳細觀點](images/dscsex.png)

在上圖中，用戶端會起始 Active Directory 物件的介面指標要求，此物件是由 ADSI 服務 (2) 所代表。 在初始化期間，服務軟體會填入已安裝之提供者程式設計識別碼的表格 (從登錄中) Progid ( "LDAP："、"Sample："、"WinNT：" 等等) 並將它們與識別適當軟體模組的相符 **CLSID** s 配對。

ADSI server 會確認 ADsPath 中是否存在 ProgID （在此案例中為 "Sample："）。 然後，它會建立系結內容，以優化此物件的進一步參考，並呼叫標準 COM 函式 [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) 來建立 COM 的標記，以用來尋找並系結至代表使用者 "Shelly" 的物件。

在下一節中，會在適當的括弧中包含範例提供者元件原始程式碼的檔案名。

如同在其他 COM 伺服器的執行中， [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) 會檢查 ProgID，並在登錄 (3) 中查閱適當的 **CLSID** ，以找出對應的提供者所提供的 class Factory 程式碼 (Cprovcf .cpp) 在適當的提供者 (中) 4。 這段程式碼會建立初始最上層物件，該物件會 [**執行 IParseDisplayName：:P arsedisplayname**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) 方法 (Cprov .cpp) 。 提供者的 **ParseDisplayName** 會解析提供者本身命名空間中的路徑。 這最後會呼叫 ADsObject，並叫用提供者元件所提供的剖析器 (Parse) ，以確認 ADsPath 對這個命名空間的語法是否正確。

**GetObject** 是在 Getobj 中定義，然後判斷要求的物件是命名空間物件、架構物件或其他類型的物件。 如果前兩個類別中的任一個，則會建立該類型的架構類別物件，並抓取適當的介面指標。 否則會從 ADsPath (建立範例目錄路徑，例如 \\ 「西雅圖 \\ Redmond \\ Shelly」，但在不同的目錄服務中，它可能必須是 \\ 「OU = 西雅圖 \\ OU = Redmond \\ CN = ) Shelly」，並將控制傳遞至 SampleDSOpenObject，以在範例資料儲存體中開啟物件，並在此情況下抓取其物件類型 (在本例中為 "User" )  (5) 。

收集資料之後，就會建立新的物件 (6) 來代表 ADsPath 所描述的專案，並抓取該物件上的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面指標。 在此情況下，會建立支援 **IUnknown** 和 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 方法的泛型 Active Directory 物件 (Cgenobj .cpp、Core .cpp) 。 CSampleDSGenObject：： AllocateGenObject 常式會讀取類型程式庫資料，為這些新物件建立適當的分派專案，以便支援 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)。

將此介面指標包裝到標記中，會完成 ResolvePathName (Cprov) 函式，並剖析顯示名稱。

基於效能考慮，會快取在此程式期間建立的所有 COM 物件，並透過系結內容進行管理。 這可改善相同物件上緊接在標記系結之後的其他作業效能。

現在會針對初始 [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) 呼叫所要求的介面識別碼，查詢此格式正確的 Active Directory 物件，並 (7) 中抓取該介面的指標，並將其從 ADSI server 回傳至用戶端 (8&9) 。 接著，用戶端會透過介面方法直接與提供者元件搭配運作，直到滿足初始要求 (10) 為止。

此外，用戶端對物件資料的要求通常會採用屬性取得和放置的要求形式，而這些要求全都是透過屬性快取的提供者執行優化 (Cprops .cpp) 。 在範例提供者元件的作業系統上的原生資料類型，以及 ADSI 所支援的 Automation [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 類型之間，以智慧方式封裝和解壓縮資料（通常包括複製和釋出結構和字串），會在屬性載入至快取 (Smpoper) 之前發生。

範例提供者元件的設計，是為了讓作業系統的實際呼叫會以邏輯方式與提供者元件隔離，以建立可攜至多個作業系統 (RegDSAPI .cpp) 的軟體。

 

 