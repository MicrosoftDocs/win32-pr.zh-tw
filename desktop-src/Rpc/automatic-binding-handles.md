---
title: 自動系結控制碼
description: 當應用程式不需要特定伺服器，且不需要維護用戶端與伺服器之間的任何狀態資訊時，自動系結控制碼會很有用。
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b619b17e44e79e623bcffa84f4938d1278a7d146d6de90547cd833e1bf091167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023438"
---
# <a name="automatic-binding-handles"></a>自動系結控制碼

當應用程式不需要特定伺服器，且不需要維護用戶端與伺服器之間的任何狀態資訊時，自動系結控制碼會很有用。 當您使用自動系結控制碼時，不需要撰寫任何用戶端應用程式程式碼來處理系結和控制碼，只要在應用程式佈建檔中指定自動系結控制碼的使用 (ACF) 。 然後，存根會定義控制碼並管理系結。

例如，您可以使用自動控制碼來執行時間戳記作業。 它不會與用戶端應用程式產生任何差異，因為它可以接受來自任何可用伺服器的時間戳記，而伺服器會提供時間戳記。

> [!Note]  
> Macintosh 平臺不支援自動控制碼。

 

您可以 \[ 在 ACF 中包含 [**auto \_ 控制碼**](/windows/desktop/Midl/auto-handle)屬性，藉以指定自動控制碼的使用方式 \] 。 時間戳記範例會使用下列 ACF：

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

當 ACF 不包含任何其他控制碼屬性時，以及遠端程式未使用明確控制碼時，MIDL 編譯器預設會使用自動控制碼。 當 ACF 不存在時，它也會使用自動控制碼作為預設值。

遠端程式是在 IDL 檔案中指定。 Auto 控制碼不能顯示為遠端程式的引數。 例如：

``` syntax
/* IDL file */
[ 
  uuid (6B29FC40-CA47-1067-B31D-00DD010662DA),
  version(1.0),
  pointer_default(unique)
]
interface autoh
{
  void GetTime([out] long * time);
  void Shutdown(void);
}
```

自動控制碼的優點是，開發人員不需要撰寫任何程式碼來管理控制碼;存根會自動管理系結。 這與 [Hello，World 範例](tutorial.md)截然不同，因為用戶端會管理 ACF 中定義的隱含基本控制碼，而且必須呼叫數個執行時間函數來建立系結控制碼。

 

 