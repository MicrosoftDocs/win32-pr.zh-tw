---
description: 系統管理安裝會在網路上建立應用程式或產品的來源映射。
ms.assetid: 40755461-317f-4764-aaa2-6b8471d52f55
title: 藉由修補系統管理映射來套用小型更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dad22d91e101d79d2bf6ecc0efc8ea9358eda2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944030"
---
# <a name="applying-small-updates-by-patching-an-administrative-image"></a>藉由修補系統管理映射來套用小型更新

[系統管理安裝](administrative-installation.md)會在網路上建立應用程式或產品的來源映射。 工作組中具有此系統管理映射存取權的使用者，可以從此來源安裝產品。 您可以透過兩個步驟來更新此工作組的應用程式：

-   首先，您可以將小型更新修補程式套用至系統管理映射。
-   其次，必須將小型更新中的變更傳播給使用者。

**將小型更新修補程式套用至系統管理映射**

1.  以 [修補程式套件](patch-packages.md)的形式取得 small update。 例如，名為 Patch 的小更新。
2.  取得系統管理映射的路徑。
3.  從命令列使用：

    **msiexec/a** 系統 *\[ 管理映射的路徑 .msi file \]* **/p** *patch .msp*

4.  這會更新系統管理映射的應用程式檔和 .msi 檔案。 如需可搭配 Msiexec.exe 使用之選項的清單，請參閱 [命令列選項](command-line-options.md)。 Windows Installer 會自動判斷系統管理映射是否使用短檔案名，並設定 [**SHORTFILENAMES**](shortfilenames.md) 屬性。
5.  產生的系統管理映射與系統管理安裝所產生的系統管理映射相同，它是使用包含更新的完整產品 cd-rom。 當新使用者從這個來源安裝應用程式時，他們會收到已更新的應用程式。

**將 small update 傳播至工作組**

-   工作組的成員會使用藉 [由重新安裝產品來套用小型更新](applying-small-updates-by-reinstalling-the-product.md)中所述的程式，從系統管理映射重新安裝應用程式，以取得變更。

 

 



