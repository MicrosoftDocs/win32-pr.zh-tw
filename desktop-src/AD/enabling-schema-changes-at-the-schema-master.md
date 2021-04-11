---
title: 在架構主機上啟用架構變更
description: 根據預設，所有 Windows 2000 網域控制站上的架構修改都會停用。
ms.assetid: 08806a9e-283c-48d9-9557-bcb9719fc13c
ms.tgt_platform: multiple
keywords:
- 在架構主機 AD 上啟用架構變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4840c9928011179ce303c83f4d00ef598f38eb64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931893"
---
# <a name="enabling-schema-changes-at-the-schema-master"></a><span data-ttu-id="73868-104">在架構主機上啟用架構變更</span><span class="sxs-lookup"><span data-stu-id="73868-104">Enabling Schema Changes at the Schema Master</span></span>

<span data-ttu-id="73868-105">根據預設，所有 Windows 2000 網域控制站上的架構修改都會停用。</span><span class="sxs-lookup"><span data-stu-id="73868-105">By default, schema modification is disabled on all Windows 2000 domain controllers.</span></span> <span data-ttu-id="73868-106">更新架構的能力是由架構主機網域控制站上的下列登錄值所控制：</span><span class="sxs-lookup"><span data-stu-id="73868-106">The ability to update the schema is controlled by the following registry value on the schema master domain controller:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            NTDS
               Parameters
                  Schema Update Allowed
```

<span data-ttu-id="73868-107">此登錄值為 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="73868-107">This registry value is a **REG\_DWORD** value.</span></span> <span data-ttu-id="73868-108">如果此值不存在或包含零 (0) ，則會停用架構修改。</span><span class="sxs-lookup"><span data-stu-id="73868-108">If this value is not present or contains zero (0), then schema modification is disabled.</span></span> <span data-ttu-id="73868-109">如果這個值存在且包含零以外的值，則會啟用架構修改。</span><span class="sxs-lookup"><span data-stu-id="73868-109">If this value is present and contains a value other than zero, then schema modification is enabled.</span></span>

<span data-ttu-id="73868-110">[架構管理員] MMC 嵌入式管理單元讓使用者能夠手動啟用或停用架構修改。</span><span class="sxs-lookup"><span data-stu-id="73868-110">The Schema Manager MMC snap-in provides the user with the ability to manually enable or disable schema modification.</span></span> <span data-ttu-id="73868-111">您可以藉由在架構主機網域控制站上修改此登錄值，以程式設計方式啟用或停用架構修改。</span><span class="sxs-lookup"><span data-stu-id="73868-111">Schema modification can be enabled or disabled programmatically by modifying this registry value on the schema master domain controller.</span></span>

<span data-ttu-id="73868-112">下列 c + + 函式顯示如何判斷架構是否可以在指定的架構主機上修改。</span><span class="sxs-lookup"><span data-stu-id="73868-112">The following C++ function shows how to determine if the schema can be modified on a specified schema master.</span></span>


```C++
HRESULT IsSchemaUpdateEnabled(
    LPTSTR pszSchemaMasterComputerName, 
    BOOL *pfEnabled)
{
    *pfEnabled = FALSE;
  
    LPTSTR szPrefix = "\\\\";
    LPTSTR pszPath = new TCHAR[lstrlen(szPrefix) + 
        lstrlen(pszSchemaMasterComputerName) + 1];
    if(!pszPath)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = E_FAIL;
    LONG lReturn;
    HKEY hKeyMachine;

    tcscpy_s(pszPath, szPrefix);
    tcscat_s(pszPath, pszSchemaMasterComputerName);
    lReturn = RegConnectRegistry(
        pszPath, 
        HKEY_LOCAL_MACHINE, 
        &hKeyMachine);
    
    delete [] pszPath;

    if (ERROR_SUCCESS == lReturn)
    {
        HKEY hKeyParameters;
        LPTSTR szKeyPath = 
          TEXT("System\\CurrentControlSet\\Services\\NTDS\\Parameters");
        LPTSTR szValueName = TEXT("Schema Update Allowed");

        lReturn = RegOpenKeyEx(
            hKeyMachine, 
            szKeyPath, 
            0, 
            KEY_READ, 
            &hKeyParameters);
        if (ERROR_SUCCESS == lReturn)
        {
            DWORD dwType;
            DWORD dwValue;
            DWORD dwSize;

            dwSize = sizeof(dwValue);
            lReturn = RegQueryValueEx(
                hKeyParameters, 
                szValueName, 
                0, 
                &dwType, 
                (LPBYTE)&dwValue, 
                &dwSize);
            if (ERROR_SUCCESS == lReturn)
            {
                *pfEnabled = (0 != dwValue);
                
                hr = S_OK;
            }
            
            RegCloseKey(hKeyParameters);
        }
    
        RegCloseKey(hKeyMachine);
    }
  
    return hr;
}
```



<span data-ttu-id="73868-113">下列 c + + 函式顯示如何在指定的架構主機上啟用或停用架構修改。</span><span class="sxs-lookup"><span data-stu-id="73868-113">The following C++ function shows how to enable or disable schema modification on a specified schema master.</span></span>


```C++
HRESULT EnableSchemaUpdate(
    LPTSTR pszSchemaMasterComputerName, 
    BOOL fEnabled)
{
    
    LPTSTR szPrefix = "\\\\";
    LPTSTR pszPath = new TCHAR[lstrlen(szPrefix) + 
        lstrlen(pszSchemaMasterComputerName) + 1];
    if(!pszPath)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = E_FAIL;
    LONG lReturn;
    HKEY hKeyMachine;

    strcpy_s(pszPath, szPrefix);
    strcat_s(pszPath, pszSchemaMasterComputerName);
    lReturn = RegConnectRegistry(
        pszPath, 
        HKEY_LOCAL_MACHINE, 
        &hKeyMachine);
    
    delete [] pszPath;

    if (ERROR_SUCCESS == lReturn)
    {
        HKEY hKeyParameters;
        LPTSTR szRelKeyPath = 
          TEXT("System\\CurrentControlSet\\Services\\NTDS\\Parameters");
        LPTSTR szValueName = TEXT("Schema Update Allowed");

        lReturn = RegOpenKeyEx(
            hKeyMachine, 
            szRelKeyPath, 
            0, 
            KEY_SET_VALUE, 
            &hKeyParameters);
        if (ERROR_SUCCESS == lReturn)
        {
            DWORD dwValue;
            DWORD dwSize;

            if(fEnabled)
            {
                dwValue = 1;
            }
            else
            {
                dwValue = 0;
            }
            
            dwSize = sizeof(dwValue);
            lReturn = RegSetValueEx(
                hKeyParameters, 
                szValueName, 
                0L, 
                REG_DWORD, 
                (LPBYTE)&dwValue, 
                dwSize);
            if (ERROR_SUCCESS == lReturn)
            {
                hr = S_OK;
            }
            
            RegCloseKey(hKeyParameters);
        }
    
        RegCloseKey(hKeyMachine);
    }
    
    return hr;
}
```



 

 




