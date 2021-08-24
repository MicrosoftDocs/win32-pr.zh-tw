---
description: Active Directory 是 Windows 的目錄服務，也是 Windows 分散式網路的基礎。
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: 存取 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43a5e60899e07335795d9728045f1e53876b013bb62c85176479fa7953ac45d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131961"
---
# <a name="accessing-active-directory"></a>存取 Active Directory

Active Directory 是 Windows 的目錄服務，也是 Windows 分散式網路的基礎。 您可以使用 Active Directory 來找出電腦網路網域中的物件，例如使用者、安全性原則、印表機、分散式元件及其他資源。 名稱 Active Directory 指的是目錄服務和目錄本身。

> [!Note]  
> 如需有關在特定作業系統上支援和安裝此元件的詳細資訊，請參閱 [WMI 元件的作業系統可用性](operating-system-availability-of-wmi-components.md)。

 

Windows 藉由建立一組包含在 Active Directory 中的類別和物件的參考，讓 Active Directory 可透過 WMI 存取。 藉由透過 WMI 存取目錄服務提供者，您可以建立啟用 WMI 的應用程式，以存取 Active Directory 中包含的豐富資訊。

使用這些介面，您可以：

-   取出類別和實例。
-   列舉類別和實例。
-   建立新的實例。
-   修改現有的實例。
-   刪除現有的實例。
-   查詢 Active Directory。

下列主題可協助您搭配使用 Active Directory 與 WMI：

-   [使用適當的 Active Directory 語法](using-the-proper-active-directory-syntax.md)
-   [將 Active Directory 對應至 WMI](mapping-active-directory-to-wmi.md)

 

 



