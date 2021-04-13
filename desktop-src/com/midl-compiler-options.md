---
title: MIDL 編譯器選項
description: MIDL 編譯器選項
ms.assetid: a78505cf-cda6-4b41-abd1-2609aec4dcb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e219daa345ad3140b78db8fdfc3de1d28678120
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316564"
---
# <a name="midl-compiler-options"></a>MIDL 編譯器選項

您可以使用下列命令列選項來覆寫 MIDL 編譯器的一些預設行為，並選擇適合您應用程式的優化。 如需 MIDL 命令列選項的完整清單，請參閱 [midl Command-Line 參考](/windows/desktop/Midl/midl-command-line-reference)。



| 命令列參數                                       | Description                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**/acf**](/windows/desktop/Midl/-acf)<br/>                          | 用來提供明確的 ACF 檔案名。 此參數也可讓您在 IDL 和 ACF 檔中使用不同的介面名稱。<br/>                                                                                                       |
| [**/dlldata**](/windows/desktop/Midl/-dlldata)<br/>                  | 指定為 proxy DLL 產生之 DLL 資料檔案的檔案名。 預設檔案名為 Dlldata.c .c。<br/>                                                                                                                              |
| [**/env**](/windows/desktop/Midl/-env)<br/>                          | 指示 MIDL 產生存根或目標環境的類型程式庫。<br/>                                                                                                                                                            |
| [**/header**](/windows/desktop/Midl/-header)、 [ **/h**](/windows/desktop/Midl/-h)<br/> | 指定介面標頭檔的名稱。 預設名稱是具有 .h 副檔名之 IDL 檔案的名稱。<br/>                                                                                                                       |
| [**/iid**](/windows/desktop/Midl/-iid)<br/>                          | 指定覆寫 COM 介面之預設介面識別碼檔案名的介面識別碼檔案名。<br/>                                                                                                              |
| [**/lcid**](/windows/desktop/Midl/-lcid)<br/>                        | 提供完整的 DBCS 支援，讓您可以在輸入檔、檔案名和目錄路徑中使用國際字元。<br/>                                                                                                          |
| [**/no \_ 格式 \_ 選擇**](/windows/desktop/Midl/-no-format-opt)<br/>    | 根據預設，若要減少程式碼大小，MIDL 會排除重複的描述項。 此參數會關閉此優化行為。<br/>                                                                                                               |
| [**/Oi**](/windows/desktop/Midl/-oi)、 **/Oic**、 **/Oif**<br/>        | 指示 MIDL 使用完全解讀的封送處理方法。 /Oic 和/Oicf 參數可提供額外的效能增強功能。<br/>                                                                                                   |
| [**/out**](/windows/desktop/Midl/-out)<br/>                          | 指定 MIDL 編譯器寫入輸出檔的目錄。 您可以使用磁碟機號、絕對路徑名稱或兩者來指定輸出目錄。 預設值是 MIDL 將檔案寫入至目前的目錄。<br/> |
| [**/proxy**](/windows/desktop/Midl/-proxy)<br/>                      | 針對 COM 介面指定介面 Proxy 檔案的名稱。 預設名稱是 IDL 檔案加上 " \_ p. c" 的名稱。<br/>                                                                                                            |
| [**/tlb**](/windows/desktop/Midl/-tlb)<br/>                          | 指定類型程式庫檔案的名稱。 預設名稱是 IDL 檔案的，副檔名為 .tlb。<br/>                                                                                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MIDL 編譯](midl-compilation.md)
</dt> </dl>

 

