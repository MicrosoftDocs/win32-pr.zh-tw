---
title: 未知的使用者類型
description: 未知的使用者類型
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ce5ee88d36399187bab24ce51f0ef1c3c074182f98ce30ff6dc7d370992ffd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129460"
---
# <a name="unknown-user-types"></a>未知的使用者類型

您可以藉由新增下列登錄機碼來簡化產品當地語系化：

**HKEY \_本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ OLE2** \\ **UnknownUserType**  =  *usertype*

此索引鍵可讓函式傳回指定的字串，而不是預設值 "Unknown"，讓當地語系化人員指定不同語言的使用者類型。

COM 預設處理常式的 [**IOleObject：： GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) 執行會藉由呼叫 [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)來檢查登錄。 如果在登錄中找不到物件的類別，則會傳回物件之 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) 實例的使用者類型。 如果在物件的 **IStorage** 實例中找不到類別，則會傳回字串 "Unknown"。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊 COM 應用程式](registering-com-applications.md)
</dt> </dl>

 

 