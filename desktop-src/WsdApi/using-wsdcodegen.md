---
description: 說明使用 WsdCodeGen 建立 WSDAPI 應用程式的流程。
ms.assetid: 8f172e2c-4cd1-4108-9c8d-01a731aca83b
title: 使用 WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6395d39a84415cc56e66949ea82ef7a1acd9fc009b7e1b2c93fa2712e8a81a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463168"
---
# <a name="using-wsdcodegen"></a>使用 WsdCodeGen

**使用 WsdCodeGen 建立 WSDAPI 應用程式**

1.  在 WSDL 檔案中定義裝置主機的功能合約。
2.  使用 WsdCodeGen 產生設定檔。 如需詳細資訊，請參閱 [WsdCodeGen 設定檔](wsdcodegen-configuration-file.md) 和 [WsdCodeGen 命令列語法](wsdcodegen-command-line-syntax.md)。
3.  開啟產生的設定檔，並視需要修改檔案。 如果您要建立用戶端應用程式，則不需要修改或修改。 如果您要建立主應用程式，請將使用者專屬的設定元素 (例如 [ [**製造商**](manufacturer.md) ] 和 [ [**modelName**](modelname.md) ]) 。
4.  使用 WsdCodeGen 產生程式碼，並提供設定檔做為輸入。 如需詳細資訊，請參閱 [WsdCodeGen 命令列語法](wsdcodegen-command-line-syntax.md)。
5.  使用產生的程式碼來建立用戶端、主機或兩者。

Windows SDK 包含一些範例 WSDL 檔案、WsdCodeGen 設定檔案和產生的程式碼。 如需詳細資訊，請參閱 [WSDAPI 範例](wsdapi-samples.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WSDAPI 範例](wsdapi-samples.md)
</dt> </dl>

 

 



