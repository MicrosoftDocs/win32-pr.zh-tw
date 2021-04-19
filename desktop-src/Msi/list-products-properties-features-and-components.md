---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiLstPrd.vbs。 範例腳本會連接到安裝程式物件，並列舉已註冊的產品和產品資訊。
ms.assetid: 13615dc2-ebc7-4536-9dd8-9bb1dbf3cfaf
title: 列出產品、屬性、功能和元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20d2f563efad42108f763b909e7a1118e255dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972230"
---
# <a name="list-products-properties-features-and-components"></a>列出產品、屬性、功能和元件

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiLstPrd.vbs。 範例腳本會連接到 [**安裝程式**](installer-object.md) 物件，並列舉已註冊的產品和產品資訊。

這個範例示範如何使用：

-   [**ProductInfo 屬性**](installer-productinfo.md)
-   [**ProductState 屬性 (安裝程式物件)**](installer-productstate-property.md)
-   [**Products 屬性**](installer-products.md)
-   [**Features 屬性**](installer-features.md)
-   [**FeatureParent 屬性**](installer-featureparent.md)
-   [**FeatureState 屬性**](installer-featurestate.md)
-   [**元件屬性**](installer-components.md)
-   [**ComponentClients 屬性**](installer-componentclients.md)
-   [**ComponentPath 屬性**](installer-componentpath.md)
-   [**LastErrorRecord 方法**](installer-lasterrorrecord.md)
-   [](installer-registryvalue.md) [**安裝程式物件** 的 RegistryValue 方法](installer-object.md)

您將需要 CScript.exe 或 WScript.exe 版本的 Windows Script Host 才能使用此範例。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令列。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[ \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**cscript WiLstPrd.vbs \[ 產品名稱 \] \[ 選項\]**

指定不區分大小寫的產品名稱或已安裝或已公告產品的產品識別碼 GUID。 如果未指定任何產品或選項，安裝程式會列出系統上安裝或公告的所有產品。

請注意，這些選項不是參數，因此您不應該在命令列上以斜線 (/) 作為前置詞。 您可以串連字母來結合下列選項。 例如，"pc" 可列出產品的屬性和已安裝的元件。



| 選項               | Description                                                                                                                           |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| 未指定任何選項 | 列出產品的屬性。                                                                                                        |
| p                    | 列出產品的屬性。                                                                                                        |
| f                    | 列出產品的功能、功能父系和安裝狀態                                                                 |
| c                    | 列出產品的已安裝元件。                                                                                              |
| d                    | 列出 [products **Software Microsoft Windows CurrentVersion shareddll for products Software of Software] 元件的 [HKLM \\ Software \\ Microsoft \\ Windows \\ \\** ] 下的值。 |



 

如需詳細資訊，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md) ，以取得其他腳本範例。 如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 



