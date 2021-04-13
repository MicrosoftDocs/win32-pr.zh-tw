---
title: /app_config 參數
description: /App \_ config 參數會選取應用程式設定模式，可讓您在 IDL 檔案中使用某些 ACF 關鍵字。 使用這個 MIDL 編譯器參數，您可以省略 ACF，並在單一 IDL 檔案中指定介面。
ms.assetid: 8d12a0ed-7eaa-4ebc-a961-b726aefefadc
keywords:
- /app_config switch MIDL
topic_type:
- apiref
api_name:
- /app_config
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717d5234bd419fec7107a6d983ece026b4558935
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373241"
---
# <a name="app_config-switch"></a>/app \_ config 參數

**/App \_ config** 參數會選取應用程式設定模式，可讓您在 IDL 檔案中使用某些 ACF 關鍵字。 使用這個 MIDL 編譯器參數，您可以省略 ACF，並在單一 IDL 檔案中指定介面。

``` syntax
midl /app_config
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

Microsoft RPC 支援在 IDL 檔案中使用下列 ACF 屬性：

-   隱含 \_ 控制碼
-   自動 \_ 處理
-   明確 \_ 控制碼

Microsoft RPC 的未來版本可能會支援在 IDL 檔案中使用其他 ACF 屬性。 **/App \_ config** 選項代表憑證-DCE 規格的 Microsoft 擴充功能，因此與 [**/osf**](-osf.md)選項互斥。

如需 **/app \_ config** 參數的相關詳細資訊，請參閱 [應用程式佈建檔 (ACF)](application-configuration-file-acf-.md) 和 [介面定義 (IDL)](interface-definition-idl-file.md)檔。

## <a name="examples"></a>範例

**midl/app \_ config 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




