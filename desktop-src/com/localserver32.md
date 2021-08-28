---
title: LocalServer32
description: 指定32位本機伺服器應用程式的完整路徑。
ms.assetid: 5d922230-f53d-4bf9-be50-c8c00f45b7a8
keywords:
- LocalServer32 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105cb352ffa3833c59e5ee8d042689e82e77b29dbcea7e49608d0047876bdd37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859398"
---
# <a name="localserver32"></a>LocalServer32

指定32位本機伺服器應用程式的完整路徑。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer32
         (Default) = path
         ServerExecutable = path
```

## <a name="remarks"></a>備註

從 Windows Server 2003 開始支援的 **ServerExecutable** 值是 **REG \_ SZ** 型別，可搭配 **LocalServer32** 子機碼使用，以避免在使用 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)函數時出現任何混淆。 **LocalServer32** 指定要啟動的 COM 伺服器應用程式的位置，這項資訊會以 **CreateProcess** 的第一個參數 *lpApplicationName* 來傳遞。 根據 **CreateProcess** 的執行，這項資訊可能不明確。 基於這個理由，如果指定 **ServerExecutable** ，COM 會將 **ServerExecutable** 的命名值傳遞給 **CreateProcess** 的 *lpApplicationName* 參數。 如果未指定 **ServerExecutable** ，COM 會傳遞 **Null** 做為 **CreateProcess** 第一個參數的值。

若要協助提供系統安全性，請在路徑中使用加上引號的字串，以指出可執行檔尾和引數的開始位置。 例如，不要將下列路徑指定為 **LocalServer32** 專案：

"C： \\ Program files \\ Company files \\Application.exe param1 param2"

使用下列語法指定路徑：

" \\ " C： \\ Program Files \\ Company files \\Application.exe\\ "param1 param2"

COM 會將 "-內嵌" 旗標附加至字串，因此使用旗標的應用程式需要剖析整個字串並檢查內嵌旗標。

當 COM 啟動32位本機伺服器時，伺服器必須在使用者所設定的經過時間內註冊類別物件。 根據預設，經過時間值必須至少為5分鐘（以毫秒為單位），但不能超過30天的毫秒數。 應用程式通常不應設定此值，其位於 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ COM2 \\ ServerStartElapsedTime** 專案中。

32位本機伺服器的必要專案為 [**InprocHandler32**](inprochandler32.md)、 [**LocalServer**](localserver.md)、 **LocalServer32** 和可 [**插入**](insertable.md)。

如果容器正在搜尋本機伺服器的登錄，則32位本機伺服器的優先順序會高於16位本機伺服器。

如果您要將類別實作為服務，您應該要注意， [**LocalService**](localservice.md) 名稱值是用於本機和遠端啟用之 **LocalServer32** 索引鍵的喜好設定。如果 **LocalService** 存在且參考有效的服務，則會忽略 **LocalServer32** 索引鍵。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**LocalServer**](localserver.md)
</dt> <dt>

[**LocalService**](localservice.md)
</dt> </dl>

 

 