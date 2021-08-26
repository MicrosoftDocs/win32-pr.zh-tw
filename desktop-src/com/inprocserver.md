---
title: InprocServer
description: 指定同進程伺服器 DLL 的路徑。
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- InprocServer 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b6cd1c7ab32733687292f01ddb48167c68243c62345fb17af3b6533a5cb454d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029888"
---
# <a name="inprocserver"></a>InprocServer

指定同進程伺服器 DLL 的路徑。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer
         (Default) = path
```

## <a name="remarks"></a>備註

**InprocServer** 專案對可插入的類別而言相當罕見。

同進程伺服器目前使用 **InprocServer** 登錄專案註冊。 32位和64位的同進程伺服器應該使用 [**InprocServer32**](inprocserver32.md) 專案。 如果容器正在搜尋內含式伺服器的登錄，16位版本的優先順序會是16位容器，而32位版本的優先順序會與32位容器相同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**InprocServer32**](inprocserver32.md)
</dt> </dl>

 

 




