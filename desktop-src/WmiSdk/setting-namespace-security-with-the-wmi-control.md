---
description: WMI 控制項是位於主控台的 MMC 嵌入式管理單元，可用來在本機電腦上手動設定 WMI 命名空間安全性。 您也可以設定腳本的預設命名空間。
ms.assetid: 87c23919-c482-4278-b005-894a8ac21da4
ms.tgt_platform: multiple
title: 使用 WMI 控制項設定命名空間安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e8b6ed7c45b6b0d107f7f4e4b92f31f504900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981041"
---
# <a name="setting-namespace-security-with-the-wmi-control"></a>使用 WMI 控制項設定命名空間安全性

WMI 控制項是位於 **主控台** 的 MMC 嵌入式管理單元，可用來在本機電腦上手動設定 WMI 命名空間安全性。 您也可以設定腳本的預設命名空間。


下列程式說明如何找出 WMI 控制項。

**找出 WMI 控制項**

1.  在 [ **主控台** 中，按兩下 [系統 **管理工具**]。
2.  在 [系統管理工具] 視窗中，按兩下 [電腦管理]。
3.  在 [ **電腦管理** ] 視窗中，展開 [ **服務和應用程式** ] 樹狀結構，然後按兩下 [ **WMI] 控制項**。
4.  以滑鼠右鍵按一下 [ **WMI 控制** ] 圖示，然後選取 [ **屬性**]。

下列程式說明如何使用 WMI 控制項，將命名空間的安全性設定為範本，然後以程式設計方式取得安全性設定，以設定其他命名空間的安全性。

**使用 WMI 控制項設定命名空間安全性**

1.  使用受控物件格式 (MOF) 程式碼來建立新的命名空間。
2.  執行 WMI 控制項，在新的命名空間上設定安全性。 在 [ **開始** ] 功能表上，按一下 [ **執行** ]，然後輸入 **wmimgmt.msc** ，或查看 [找出 WMI 控制項](#)。
3.  在 [ **Wmi 控制** ] 窗格中，以滑鼠右鍵按一下 [ **wmi 控制**]，選擇 [ **屬性**]，然後選取 [ **安全性** ] 索引標籤。
4.  流覽至新的命名空間，按一下 [ **安全性**]，然後設定命名空間的群組和許可權。

您也可以使用 Windows Management Instrumentation Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) 來設定命名空間安全性。 如需詳細資訊，請參閱 [**wmic**](wmic.md)。

## <a name="setting-the-default-namespace-for-scripts"></a>設定腳本的預設命名空間

如果腳本在連接至 WMI 時未明確連接到命名空間，則 WMI 會使用此控制項中指定的預設命名空間。 在登錄專案中也可以找到預設值，如下所示：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         WBEM
            Scripting
               Default
                  Namespace
```

由於預設的命名空間很容易變更，不論是使用此控制項，或是藉由呼叫 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)的方法以程式設計方式進行，請在透過 [**wbemscripting.swbemlocator 或. ConnectServer**](swbemlocator-connectserver.md)[的呼叫](constructing-a-moniker-string.md)連接至 WMI 時，指定命名空間。 如需詳細資訊，請參閱 [建立 WMI 腳本](creating-a-wmi-script.md)

**設定腳本的預設命名空間**

1.  在 [ **WMI 控制項屬性** ] 視窗中，選擇 [ **Advanced （Advanced** ）] 索引標籤。
2.  按一下 [ **變更** ] 按鈕，然後選取要做為預設值的命名空間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定命名空間安全描述項](setting-namespace-security-descriptors.md)
</dt> </dl>

 

 
