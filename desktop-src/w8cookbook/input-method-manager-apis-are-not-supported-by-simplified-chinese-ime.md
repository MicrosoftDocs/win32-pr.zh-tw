---
title: 簡體中文 IME 不支援輸入方法管理員 Api
description: 簡體中文 IME 不支援輸入方法管理員 Api
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0454df8df722992e321fd7fc6bd745382ea215116b2fd5a7797f2032a9c7e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935408"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a>簡體中文 IME 不支援輸入方法管理員 Api

## <a name="platforms"></a>平台

<dl> 用戶端-Windows 8。1  
Windows Server 2012 R2  
</dl>

## <a name="description"></a>描述

Windows 8.1 中的簡體中文 Ime 不支援下列輸入方法管理員 Api：

-   IFECommon 介面
-   IFEDictionary 介面
-   IFELanguage 介面
-   IImePad 介面
-   IImePadApplet 介面
-   IImeSpecifyApplets 介面

## <a name="manifestations"></a>表現

使用這些 Api 的函式不適用於簡體中文 IME。

## <a name="solution"></a>解決方案

應用程式必須經過設計，使用者才能完成所需的工作，而不需使用指定的 API。

## <a name="resources"></a>資源

-   [輸入方法管理員介面](../intl/input-method-manager-interfaces.md)
-   [IFECommon](/windows/win32/api/msime/nn-msime-ifecommon)
-   [IFECommon 介面](/windows/win32/api/msime/nn-msime-ifecommon)
-   [IFEDictionary 介面](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [IFELanguage](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [IImePad](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [IImePadApplet](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [IimePlugInDictDictionaryList](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [IImeSpecifyApplets](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 