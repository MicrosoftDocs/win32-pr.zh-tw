---
title: 使用 JAVA/COM 編寫 ADSI 程式設計
description: 您可以使用 Microsoft virtual machine for JAVA (Microsoft VM) 和 Microsoft JAVA 編譯器，從 JAVA/COM 應用程式存取所有透過任何 ADSI COM 元件公開的 ADSI 功能。
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- 使用 JAVA/COM AD 撰寫 ADSI 程式設計
- ADSI ADSI、使用、JAVA/COM 程式設計
- ADSI ADSI，範例程式碼 JAVA
- ADSI ADSI，範例程式碼 JAVA，系結至 ADSI 物件，並在該物件上叫用方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4778d1d1f71920f880fe38a71874283f7cd8628ae0376b3f9ce227305ab184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178972"
---
# <a name="programming-adsi-with-javacom"></a>使用 JAVA/COM 編寫 ADSI 程式設計

您可以使用 Microsoft virtual machine for JAVA (Microsoft VM) 和 Microsoft JAVA 編譯器，從 JAVA/COM 應用程式存取所有透過任何 ADSI COM 元件公開的 ADSI 功能。 下列 JAVA 程式碼範例顯示系結至 ADSI 物件，並在該物件上叫用方法所需的元素。 必要的 ADSI API 函數和物件方法會透過 Activeds.dll 公開。


```C++
import activeds.*;       // ADSI COM Wrapper classes
import com.ms.com.*;     // to use _Guid data type in COM.

public Class SimpleADSI 
{
    IADs obj;
    String path = "WinNT://domain/machine,computer";
    _Guid riid = IADs.iid;
    public static void main(String args[]) 
    {
        try 
        {
            obj = (IADs)ADsGetObject(path, riid);
            System.out.println( "Object name:  " + obj.getName() );
            System.out.println( "      class:  " + obj.getSchema() );
            System.out.println( "    ADsPath:  " + obj.getADsPath() );
            System.out.println( "     parent:  " + obj.getParent() );
        }
        catch (Exception e) 
        {
            System.out.println( "SimpleADSI Error: " + e.toString() );
        }
    }

    /** @dll.import("activeds", ole) */
    private static native IUnknown ADsGetObject(String path, _Guid riid);
}
```



第一個 **import** 語句中的引數是指封裝于 Activeds.dll 中的 JAVA 包裝函式類別。 使用 Visual c + + 來建立包裝函式類別，並將它們包含在您的專案中，請遵循下列程式。

**建立包裝函式類別，並將它們包含在您的專案中**

1.  在 Visual c + + 專案中，選取 [ **Project** ] 功能表中的 [**加入 Com 包裝** 函式 ...]。
2.  從 [COM 包裝函式] 對話方塊的 [ **已安裝的元件** ] 中選取 [Active DS 類型程式庫]。 如果清單方塊中未顯示類型程式庫，請按一下 [ **流覽 ...]** 按鈕，流覽至儲存 Activeds 的目錄，然後選取類型程式庫。

Visual c + + 會建立 JAVA 包裝函式類別的 activeds 封裝，並將封裝包含在專案的預設路徑中。 如需詳細資訊，請參閱 Visual c + + 視窗的 **Project 探索**] 窗格中的 activeds 封裝。

若要取得無法 cocreated 的 ADSI 物件，請使用其中一個已公開的 ADSI API 函式，例如 [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) 或 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)，這些函式也會封裝在 Activeds.dll 中。 Microsoft J/Direct 提供這些和其他原生 Api 的存取權。 上述程式碼範例的最後兩行說明這一點。

在編譯時，請確定已啟用 Microsoft 語言延伸模組。 若要這樣做，請從 [Visual j + + 專案] 視窗中的 [ **Project** ] 功能表選取 [ **<project> 屬性 ...** ]。 然後，按一下 [ **<project> 屬性**] 對話方塊中的 [**編譯**] 索引標籤。 清除 [ **停用 Microsoft 語言擴充** 功能] 核取方塊。 如果是從命令列編譯，請使用 "/x-" 參數，例如：

**jvc/x-SimpleADSI .java**

最後，為了讓虛擬機器載入 COM 元件，必須在系統路徑上看到動態連結程式庫 (DLL) 。 如果傳回 "UnsatisfiedLinkError" 錯誤，請將路徑設定為包含所需 DLL 的路徑。 例如，如果 Activeds.dll 已安裝在 c： \\ adsi lib 中 \\ ，請從命令列發出下列命令：

**set PATH =% PATH%;c： \\ adsi \\ lib**

 

 




