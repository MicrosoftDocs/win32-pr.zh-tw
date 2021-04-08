---
description: 提供安全性內容的安全通道特定資訊。
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: 查詢 Schannel 內容的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6951aee242b12cc5fcc7f9c52de7e793c2e92733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112168"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a>查詢 Schannel 內容的屬性

[**QueryCoNtextAttributes (schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw)函數提供 [*安全性內容的安全*](../secgloss/s-gly.md)通道特定資訊。 大部分的資訊最初是在使用用戶端 [**InitializeSecurityCoNtext (schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) 或伺服器 [**AcceptSecurityCoNtext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函式建立內容時所指定。 取得用來建立內容之認證的控制碼時，會指定一些資訊。 如需詳細資訊，請參閱 [取得 Schannel 認證](obtaining-schannel-credentials.md)。

 

 
