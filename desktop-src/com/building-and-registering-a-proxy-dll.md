---
title: 建立和註冊 Proxy DLL
description: 如果您為應用程式選擇 proxy/存根封送處理，則必須編譯並連結 MIDL 產生的 .c 和 .h 檔案，以建立 proxy DLL，而且必須在系統登錄中輸入該 DLL，才能讓用戶端找到您的介面。
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d4cafbe2be56d9e9a02a451e3daf905496c424
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826803"
---
# <a name="building-and-registering-a-proxy-dll"></a>建立和註冊 Proxy DLL

如果您為應用程式選擇 proxy/存根封送處理，則必須編譯並連結 MIDL 產生的 .c 和 .h 檔案，以建立 proxy DLL，而且必須在系統登錄中輸入該 DLL，才能讓用戶端找到您的介面。 MIDL 產生的檔案 Dlldata.c 包含必要的常式，以及用來建立和註冊 proxy/stub DLL 的其他資訊。

建立 DLL 的第一個步驟是為連結器撰寫模組定義檔，如下列範例所示：

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

或者，您可以在 makefile 的連結命令列上指定這些匯出的函式。

匯出的函式會在 Rpcproxy 中宣告，其中 Dlldata.c 包含，而預設的實作為 RPC 執行時間程式庫的一部分。 COM 會使用這些函式來建立 class factory、卸載 Dll， (確定沒有任何物件或鎖定存在) 、取得 proxy DLL 的相關資訊，以及自行註冊和取消註冊 proxy DLL。 若要利用這些預先定義的函式，您必須在編譯 Dlldata.c 和範例 p .c 檔案時，叫用 Cpreprocessor/D (或-D) 選項 \_ ，如下列 makefile 所示：

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcndr.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJS) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
 
```

如果您未在編譯時期指定這些預處理器定義，則不會自動定義這些函數。  (亦即，Rpcproxy 中的宏會展開為 nothing。 ) 您必須在另一個原始程式檔中明確定義它們，也就是它的模組也會包含在 C 編譯器命令列的最終連結和編譯中。

當 \_ 定義 REGISTER proxy \_ DLL 時，Rpcproxy 會針對具有 PROXY clsid = guid 的其他條件式編譯控制項提供 \_ ，proxy \_ clsid \_ =*guid 的明確值*，以及輸入 \_ 首碼 =*前置詞字串*。 在 MIDL 程式設計人員手冊中， [Proxy/存根的 C-編譯器定義](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) 中會更詳細地說明這些巨集定義。

## <a name="manually-registering-the-proxy-dll"></a>手動註冊 Proxy DLL

如果基於某些原因而無法使用預設 proxy 存根登錄常式，您可以使用 Regedt32.exe，將下列專案新增至系統登錄以手動註冊 DLL。

```
HKEY_CLASSES_ROOT
   Interface
      iid
         (Default) = ICustomInterfaceName
         ProxyStubClsid32 = {clsid}
```

```
HKEY_CLASSES_ROOT
   CLSID
      clsid
         (Default) = ICustomInterfaceName_PSFactory
         InprocServer32 = proxstub.dll
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[C-Proxy/Stub 的編譯器定義](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[註冊 COM 伺服器](registering-com-servers.md)
</dt> <dt>

[自我註冊](self-registration.md)
</dt> </dl>

 

 
