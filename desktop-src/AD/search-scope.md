---
title: 指定搜尋範圍
description: 您可以將搜尋範圍指定為基底、單一層級或子樹搜尋。
ms.assetid: b02354c2-7b95-4911-8ae3-4a261d3ca2d3
ms.tgt_platform: multiple
keywords:
- 指定搜尋範圍 AD
- Active Directory、搜尋、指定搜尋範圍
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ea307e349ffc91da41e72798be9c6232c9a510e2edf5563e5407d3d58ef2fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183856"
---
# <a name="specifying-the-search-scope"></a>指定搜尋範圍

您可以將搜尋範圍指定為基底、單一層級或子樹搜尋。 使用 **ads \_ SEARCHPREF \_ 搜尋 \_ 範圍** 旗標搭配 [**ads \_ SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum) 列舉的值，以指定搜尋範圍。 下列清單包含搜尋類型的描述：

-   **基底**。 基底搜尋會將搜尋限制為基底物件。 傳回的物件數目上限一律為一個。 這項搜尋有助於確認物件是否存在，以便取得群組成員資格。 例如，如果您有物件辨別名稱，而且必須根據路徑確認物件是否存在，您可以使用一層級的搜尋。 如果搜尋失敗，您可以假設物件可能已重新命名或移至不同的位置，或您已獲得關於物件的錯誤資訊。 請注意，如果您想要重新流覽物件，您應該儲存物件的全域唯一識別碼 (GUID) ，而不是分辨名稱。 GUID 一律會參考相同的物件，無論物件在目錄階層中的位置為何。
-   **一個層級**。 單一層級的搜尋僅限於基底物件的直屬子系，但會排除基底物件本身。 這項設定可以針對父物件的直屬子物件，執行目標搜尋。 例如，請考慮父物件 P1 及其直屬子系： C1、C2 和 C3。 一層搜尋會針對搜尋準則評估 C1、C2 和 C3，但不會評估 P1。 使用一層級的搜尋來列舉物件的所有子系。 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer)列舉會轉譯為一層級的搜尋。
-   **子樹**。 子樹搜尋 (或深層搜尋) 包含所有子物件以及基底物件。 您可以要求 LDAP 提供者，以對其他 LDAP 目錄服務（包括其他目錄網域或樹系）的參考。

 

 