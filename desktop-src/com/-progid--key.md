---
title: ProgID 索引鍵
description: " (ProgID) 的程式設計識別碼是可以與 CLSID 相關聯的登錄專案。 如同 CLSID，ProgID 會識別類別但精確度較低，因為它不保證是全域唯一的。"
ms.assetid: f9ef2934-0815-4a6f-9283-8f748eee083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ef64515d2dda4512af0086970cb2ab61b4830
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024462"
---
# <a name="progid-key"></a><span data-ttu-id="0d087-104">ProgID 索引鍵</span><span class="sxs-lookup"><span data-stu-id="0d087-104">ProgID Key</span></span>

<span data-ttu-id="0d087-105"> (ProgID) 的程式設計識別碼是可以與 CLSID 相關聯的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="0d087-105">A programmatic identifier (ProgID) is a registry entry that can be associated with a CLSID.</span></span> <span data-ttu-id="0d087-106">如同 CLSID，ProgID 會識別類別但精確度較低，因為它不保證是全域唯一的。</span><span class="sxs-lookup"><span data-stu-id="0d087-106">Like the CLSID, the ProgID identifies a class but with less precision because it is not guaranteed to be globally unique.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0d087-107">登錄項目</span><span class="sxs-lookup"><span data-stu-id="0d087-107">Registry Entry</span></span>

<span data-ttu-id="0d087-108">**HKEY \_本機 \_ 電腦 \\ 軟體 \\ 類別** \\ *{* ProgID *}*</span><span class="sxs-lookup"><span data-stu-id="0d087-108">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**\\ *{* ProgID *}*</span></span>



| <span data-ttu-id="0d087-109">登錄機碼</span><span class="sxs-lookup"><span data-stu-id="0d087-109">Registry key</span></span>                            | <span data-ttu-id="0d087-110">說明</span><span class="sxs-lookup"><span data-stu-id="0d087-110">Description</span></span>                                                        |
|-----------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="0d087-111">**Clsid**</span><span class="sxs-lookup"><span data-stu-id="0d087-111">**CLSID**</span></span>](clsid.md)                  | <span data-ttu-id="0d087-112">將 ProgID 與 CLSID 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="0d087-112">Associates a ProgID with a CLSID.</span></span>                                  |
| [<span data-ttu-id="0d087-113">**插入**</span><span class="sxs-lookup"><span data-stu-id="0d087-113">**Insertable**</span></span>](insertable-progid.md) | <span data-ttu-id="0d087-114">指出這個類別可在 OLE 2 容器中插入。</span><span class="sxs-lookup"><span data-stu-id="0d087-114">Indicates that this class is insertable in OLE 2 containers.</span></span>       |
| [<span data-ttu-id="0d087-115">**通訊協定**</span><span class="sxs-lookup"><span data-stu-id="0d087-115">**Protocol**</span></span>](protocol.md)            | <span data-ttu-id="0d087-116">指出 OLE 1 容器中可插入這個 OLE 2 類別。</span><span class="sxs-lookup"><span data-stu-id="0d087-116">Indicates that this OLE 2 class is insertable in OLE 1 containers.</span></span> |
| [<span data-ttu-id="0d087-117">**殼層**</span><span class="sxs-lookup"><span data-stu-id="0d087-117">**Shell**</span></span>](shell.md)                  | <span data-ttu-id="0d087-118">提供 Windows 3.1 shell 列印和檔案 **開啟** 資訊。</span><span class="sxs-lookup"><span data-stu-id="0d087-118">Provides Windows 3.1 shell printing and **File Open** information.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0d087-119">備註</span><span class="sxs-lookup"><span data-stu-id="0d087-119">Remarks</span></span>

<span data-ttu-id="0d087-120">您可以在不能使用 CLSID 的程式設計情況下使用 ProgID。</span><span class="sxs-lookup"><span data-stu-id="0d087-120">You can use a ProgID in programming situations where it is not possible to use a CLSID.</span></span> <span data-ttu-id="0d087-121">Progid 不應該出現在使用者介面中。</span><span class="sxs-lookup"><span data-stu-id="0d087-121">ProgIDs should not appear in the user interface.</span></span> <span data-ttu-id="0d087-122">Progid 不保證是唯一的，因此只能在名稱衝突可供管理時使用。</span><span class="sxs-lookup"><span data-stu-id="0d087-122">ProgIDs are not guaranteed to be unique, so they can be used only where name collisions are manageable.</span></span>

<span data-ttu-id="0d087-123">ProgID 的格式為 <*程式*>。 <*元件*>。 <*版本*>，以句號分隔，而且沒有空格，如 Word.Doc>ument 6。</span><span class="sxs-lookup"><span data-stu-id="0d087-123">The format of a ProgID is <*Program*>.<*Component*>.<*Version*>, separated by periods and with no spaces, as in Word.Document.6.</span></span> <span data-ttu-id="0d087-124">ProgID 必須符合下列需求：</span><span class="sxs-lookup"><span data-stu-id="0d087-124">The ProgID must comply with the following requirements:</span></span>

-   <span data-ttu-id="0d087-125">不能超過39個字元。</span><span class="sxs-lookup"><span data-stu-id="0d087-125">Have no more than 39 characters.</span></span>
-   <span data-ttu-id="0d087-126">除了一或多個句號之外，不包含標點符號 (包括底線) 。</span><span class="sxs-lookup"><span data-stu-id="0d087-126">Contain no punctuation (including underscores) except one or more periods.</span></span>
-   <span data-ttu-id="0d087-127">不是以數位開頭。</span><span class="sxs-lookup"><span data-stu-id="0d087-127">Not start with a digit.</span></span>
-   <span data-ttu-id="0d087-128">不同于任何 OLE 1 應用程式的類別名稱，包括相同應用程式的 OLE 1 版本（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="0d087-128">Be different from the class name of any OLE 1 application, including the OLE 1 version of the same application, if there is one.</span></span>

<span data-ttu-id="0d087-129">由於 ProgID 不應該出現在使用者介面中，因此您可以藉由呼叫 [**IOleObject：： GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)來取得可顯示的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d087-129">Because the ProgID should not appear in the user interface, you can obtain a displayable name by calling [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype).</span></span> <span data-ttu-id="0d087-130">另請參閱 [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)。</span><span class="sxs-lookup"><span data-stu-id="0d087-130">Also, see [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span></span>

<span data-ttu-id="0d087-131">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 金鑰組應至 **HKEY \_ 類別 \_ 根金鑰**，此機碼是為了與舊版 COM 相容而保留的。</span><span class="sxs-lookup"><span data-stu-id="0d087-131">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d087-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="0d087-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d087-133">**IOleObject::GetUserType**</span><span class="sxs-lookup"><span data-stu-id="0d087-133">**IOleObject::GetUserType**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> <dt>

[<span data-ttu-id="0d087-134">**OleRegGetUserType**</span><span class="sxs-lookup"><span data-stu-id="0d087-134">**OleRegGetUserType**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)
</dt> </dl>

 

 




