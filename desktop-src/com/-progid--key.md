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
# <a name="progid-key"></a>ProgID 索引鍵

 (ProgID) 的程式設計識別碼是可以與 CLSID 相關聯的登錄專案。 如同 CLSID，ProgID 會識別類別但精確度較低，因為它不保證是全域唯一的。

## <a name="registry-entry"></a>登錄項目

**HKEY \_本機 \_ 電腦 \\ 軟體 \\ 類別** \\ *{* ProgID *}*



| 登錄機碼                            | 說明                                                        |
|-----------------------------------------|--------------------------------------------------------------------|
| [**Clsid**](clsid.md)                  | 將 ProgID 與 CLSID 產生關聯。                                  |
| [**插入**](insertable-progid.md) | 指出這個類別可在 OLE 2 容器中插入。       |
| [**通訊協定**](protocol.md)            | 指出 OLE 1 容器中可插入這個 OLE 2 類別。 |
| [**殼層**](shell.md)                  | 提供 Windows 3.1 shell 列印和檔案 **開啟** 資訊。 |



 

## <a name="remarks"></a>備註

您可以在不能使用 CLSID 的程式設計情況下使用 ProgID。 Progid 不應該出現在使用者介面中。 Progid 不保證是唯一的，因此只能在名稱衝突可供管理時使用。

ProgID 的格式為 <*程式*>。 <*元件*>。 <*版本*>，以句號分隔，而且沒有空格，如 Word.Doc>ument 6。 ProgID 必須符合下列需求：

-   不能超過39個字元。
-   除了一或多個句號之外，不包含標點符號 (包括底線) 。
-   不是以數位開頭。
-   不同于任何 OLE 1 應用程式的類別名稱，包括相同應用程式的 OLE 1 版本（如果有的話）。

由於 ProgID 不應該出現在使用者介面中，因此您可以藉由呼叫 [**IOleObject：： GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)來取得可顯示的名稱。 另請參閱 [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)。

**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 金鑰組應至 **HKEY \_ 類別 \_ 根金鑰**，此機碼是為了與舊版 COM 相容而保留的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> <dt>

[**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)
</dt> </dl>

 

 




