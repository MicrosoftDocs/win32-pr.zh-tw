---
title: 與版本無關的 ProgID 金鑰
description: 將 ProgID 與 CLSID 產生關聯。 此索引鍵可用來判斷物件應用程式的最新版本。
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a0bf379a06a6a05bb69a232ef91bb9fe81dc2f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464104"
---
# <a name="version-independent-progid-key"></a><span data-ttu-id="2a330-104">與版本無關的 ProgID 金鑰</span><span class="sxs-lookup"><span data-stu-id="2a330-104">version-independent ProgID Key</span></span>

<span data-ttu-id="2a330-105">將 ProgID 與 CLSID 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="2a330-105">Associates a ProgID with a CLSID.</span></span> <span data-ttu-id="2a330-106">此索引鍵可用來判斷物件應用程式的最新版本。</span><span class="sxs-lookup"><span data-stu-id="2a330-106">This key is used to determine the latest version of an object application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="2a330-107">登錄項目</span><span class="sxs-lookup"><span data-stu-id="2a330-107">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a><span data-ttu-id="2a330-108">備註</span><span class="sxs-lookup"><span data-stu-id="2a330-108">Remarks</span></span>

<span data-ttu-id="2a330-109">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 金鑰組應至 **HKEY \_ 類別 \_ 根金鑰**，此機碼是為了與舊版 COM 相容而保留的。</span><span class="sxs-lookup"><span data-stu-id="2a330-109">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

<span data-ttu-id="2a330-110"><與 *版本無關的 ProgID*> 的格式 <*程式*>。 <*元件*>，以句號分隔，沒有空格，且沒有版本號碼。</span><span class="sxs-lookup"><span data-stu-id="2a330-110">The format for <*version-independent ProgID*> is <*program*>.<*component*>, separated by periods, no spaces, and no version number.</span></span> <span data-ttu-id="2a330-111">與版本無關的 ProgID （例如 ProgID）可以註冊為人們可讀取的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a330-111">The version-independent ProgID, like the ProgID, can be registered with a human-readable name.</span></span>

<span data-ttu-id="2a330-112">*Progid* 是類別的最新已安裝版本的 progid。</span><span class="sxs-lookup"><span data-stu-id="2a330-112">*ProgID* is the ProgID of the latest installed version of the class.</span></span>

<span data-ttu-id="2a330-113">應用程式必須在與 *版本無關的 ProgID* 金鑰下註冊與版本無關的程式設計識別碼。</span><span class="sxs-lookup"><span data-stu-id="2a330-113">Applications must register a version-independent programmatic identifier under the *version-independent ProgID* key.</span></span> <span data-ttu-id="2a330-114">與版本無關的 ProgID 指的是應用程式的類別，而且不會從版本變更為版本，而是在所有 versionsâ中的剩餘常數（例如 Microsoft Word 檔）。</span><span class="sxs-lookup"><span data-stu-id="2a330-114">The version-independent ProgID refers to the application's class and does not change from version to version, instead remaining constant across all versionsâ€”for example, Microsoft Word Document.</span></span> <span data-ttu-id="2a330-115">它會與宏語言搭配使用，並參考目前安裝的應用程式類別版本。</span><span class="sxs-lookup"><span data-stu-id="2a330-115">It is used with macro languages and refers to the currently installed version of the application's class.</span></span> <span data-ttu-id="2a330-116">與版本無關的 ProgID 必須對應至最新版本的物件應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="2a330-116">The version-independent ProgID must correspond to the name of the latest version of the object application.</span></span>

<span data-ttu-id="2a330-117">例如，當容器應用程式使用工具列按鈕建立圖表或資料表時，會使用與版本無關的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="2a330-117">For example, the version-independent ProgID is used when a container application creates a chart or table with a toolbar button.</span></span> <span data-ttu-id="2a330-118">在這種情況下，應用程式可以使用與版本無關的 ProgID 來判斷所需物件應用程式的最新版本。</span><span class="sxs-lookup"><span data-stu-id="2a330-118">In this situation, the application can use the version-independent ProgID to determine the latest version of the needed object application.</span></span>

<span data-ttu-id="2a330-119">與版本無關的 ProgID 只會由應用程式程式碼儲存和維護。</span><span class="sxs-lookup"><span data-stu-id="2a330-119">The version-independent ProgID is stored and maintained solely by application code.</span></span> <span data-ttu-id="2a330-120">當指定與版本無關的 ProgID 時， [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) 函數會傳回目前版本的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="2a330-120">When given the version-independent ProgID, the [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) function returns the CLSID of the current version.</span></span>

<span data-ttu-id="2a330-121">您可以使用 [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) 和 [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) ，在這兩種標記法之間進行轉換。</span><span class="sxs-lookup"><span data-stu-id="2a330-121">You can use [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) and [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) to convert between these two representations.</span></span>

<span data-ttu-id="2a330-122">您可以使用 [**IOleObject：： GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) 或 [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) ，將識別碼變更為可顯示的字串。</span><span class="sxs-lookup"><span data-stu-id="2a330-122">You can use [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) or [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) to change the identifier to a displayable string.</span></span>

<span data-ttu-id="2a330-123">如果未使用自訂處理常式，則專案應設定為 OLE32.DLL，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="2a330-123">If a custom handler is not used, the entry should be set to OLE32.DLL, as shown in the following example:</span></span>

```
HKEY_CLASSES_ROOT\CLSID\{00000402-0000-0000-C000-000000000046}
   InprocHandler = ole32.dll
```

## <a name="related-topics"></a><span data-ttu-id="2a330-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a330-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a330-125">**CLSIDFromProgID**</span><span class="sxs-lookup"><span data-stu-id="2a330-125">**CLSIDFromProgID**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid)
</dt> <dt>

[<span data-ttu-id="2a330-126">**ProgIDFromCLSID**</span><span class="sxs-lookup"><span data-stu-id="2a330-126">**ProgIDFromCLSID**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid)
</dt> <dt>

[<span data-ttu-id="2a330-127"><ProgID> 關鍵</span><span class="sxs-lookup"><span data-stu-id="2a330-127"><ProgID> Key</span></span>](-progid--key.md)
</dt> </dl>

 

 




