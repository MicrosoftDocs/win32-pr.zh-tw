---
title: 使用 MIDL
description: 建立和編譯 Microsoft 介面定義語言 (MIDL) 介面和遠端程序呼叫 (RPC) 。
ms.assetid: 2594e3d6-d44a-4e12-8286-b9700e67702e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ae89a740831fef28ade4c07dc6bbe2b9b68a8a154eb119f47e16b2cb68b325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010746"
---
# <a name="using-midl"></a>使用 MIDL

使用 RPC 的程式的所有介面都必須在 Microsoft 介面定義語言 (MIDL) 中定義，並使用 MIDL 編譯器進行編譯。 下列主題提供建立和編譯 MIDL 介面的簡短總覽：

-   [使用 MIDL 定義介面](#defining-an-interface-with-midl)
-   [編譯 MIDL 檔案](#compiling-a-midl-file)

如需這些主題的詳細討論，請參閱 [IDL 和 ACF](the-idl-and-acf-files.md)檔案。

## <a name="defining-an-interface-with-midl"></a>使用 MIDL 定義介面

MIDL 檔案是您可以使用文字編輯器來建立和編輯的文字檔。 如果您為介面產生 UUID，通常會將輸出儲存在範本 MIDL 檔案中。 如需 Uuid 的詳細資訊，請參閱 [產生介面 uuid](generating-interface-uuids.md)。

MIDL 中的所有介面都遵循相同的格式。 它們的開頭是包含介面屬性清單和介面名稱的標頭。 屬性以方括弧括住。 介面標頭後面接著其主體，並以大括弧括住。 下列範例會顯示簡單的介面：

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface MyInterface
{
  const unsigned short INT_ARRAY_LEN = 100;

  void MyRemoteProc( 
      [in] int param1,
      [out] int outArray[INT_ARRAY_LEN]
  );
}
```

某些通常會出現在 MIDL 介面定義中的屬性是 UUID 和介面版本號碼。 介面定義的主體必須包含介面中所有遠端程式的程式聲明。 它也可以包含介面所需之資料類型和常數的宣告。

遠端過程聲明中的所有參數都必須宣告為 \[ [**in**](/windows/desktop/Midl/in) \] 、 \[ [**out**](/windows/desktop/Midl/out-idl) \] 或 \[ **in**、 **out** \] 。 這些宣告會指定用戶端程式將資料傳遞至遠端程式、從遠端程式取得資料，或同時從兩者取得資料。 如需有關介面參數聲明的詳細資訊，請參閱 [IDL 介面主體](the-idl-interface-body.md)。

## <a name="compiling-a-midl-file"></a>編譯 MIDL 檔案

MIDL 編譯器是一種命令列工具，會隨平臺軟體發展工具組 (SDK) 自動安裝。 在命令列中輸入 **midl** 的命令，並在命令列中輸入 midl 檔案的名稱，在命令視窗中叫用它。 請確定包含 MIDL 編譯器的目錄在您的路徑中。 下列範例說明其用途：

**midl MyApp .idl**

請注意，如果檔案名具有 .idl 副檔名，就不需要包含副檔名。 您也可以使用 MIDL 編譯器 [命令列參數](/windows/desktop/Midl/midl-command-line-reference) ，方法是將它們插入 **midl** 命令和檔案名之間。 下列範例會示範這種情況：

**midl/acf MyApp. acf MyApp .idl**

在此範例中，會使用 file MyApp 作為輸入檔來執行 MIDL 編譯器。 命令列參數 **/acf** 會指示編譯器使用應用程式佈建檔， (acf 輸入的) 。 在 [IDL 和 ACF](the-idl-and-acf-files.md)檔案中，會更詳盡地討論應用程式佈建檔。

如需使用 MIDL 編譯器的詳細資訊，請參閱 [Microsoft 介面定義語言 (midl) ](/windows/desktop/Midl/midl-start-page)，其中包含下列主題的相關資訊：

-   [C-MIDL 的預處理器需求](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [C/c + +-編譯器考慮](/windows/desktop/Midl/c-c-compiler-considerations)
-   [針對 RPC 介面產生的檔案](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [MIDL 命令列參考](/windows/desktop/Midl/midl-command-line-reference)
-   [MIDL 語言參考](/windows/desktop/Midl/midl-language-reference)
-   [MIDL 編譯器錯誤和警告](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 