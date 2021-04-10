---
title: 簡體中文 IME 不支援輸入方法管理員 Api
description: 簡體中文 IME 不支援輸入方法管理員 Api
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d01d79d569ee7c72508bc217b68bcdf784f0d61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092862"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a>簡體中文 IME 不支援輸入方法管理員 Api

## <a name="platforms"></a>平台

<dl> 用戶端-Windows 8。1  
Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

Windows 8.1 中的簡體中文 Ime 不支援下列輸入方法管理員 Api：

-   IFECommon 介面
-   IFEDictionary 介面
-   IFELanguage 介面
-   IImePad 介面
-   IImePadApplet 介面
-   IImeSpecifyApplets 介面

## <a name="manifestations"></a>表現

使用這些 Api 的函式不適用於簡體中文 IME。

## <a name="solution"></a>解決方法

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

 

 